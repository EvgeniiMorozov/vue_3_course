<template>
  <div class="app">
    <post-form
        @create="createPost"
    />
    <post-list
        :posts="posts"
    />

  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  name: "App",
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'JavaScript', body: 'Описание поста'},
        {id: 2, title: 'JavaScript 2', body: 'Описание поста 2'},
        {id: 3, title: 'JavaScript 3', body: 'Описание поста 3'},
        {id: 4, title: 'JavaScript 4', body: 'Описание поста 4'},
        {id: 5, title: 'JavaScript 5', body: 'Описание поста 5'},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    },
    // можно обойтись и без этой функции
    // inputTitle(event) {
    //   this.title = event.target.value;
    // }
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}

form {
  display: flex;
  flex-direction: column;
}
</style>

<!--Single file component-->