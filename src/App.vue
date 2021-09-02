<template>
  <div>
    <div class="post" v-for="post in posts" :key="post.id">
      <div><strong>Название:</strong> {{post.title}}</div>
      <div><strong>Описание:</strong> {{post.body}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      posts: [
        {id: 1, title: 'JavaScript', body: 'Описание поста'},
        {id: 2, title: 'JavaScript 2', body: 'Описание поста 2'},
        {id: 3, title: 'JavaScript 3', body: 'Описание поста 3'},
        {id: 4, title: 'JavaScript 4', body: 'Описание поста 4'},
        {id: 5, title: 'JavaScript 5', body: 'Описание поста 5'},
      ]
    }
  },
  methods: {},
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.post {
  margin-top: 15px;
  padding: 15px;
  border: 2px solid teal;
}
</style>

<!--Single file component-->