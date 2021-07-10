<template>
<div class="app">
  <post-form @create="createPost"/>
  <post-list :posts="posts"/>
</div>
</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";

export default {
  name: "App",
  components: {
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Это название 1', body: 'Это описание 1'},
        {id: 2, title: 'Это название 2', body: 'Это описание 2'},
        {id: 3, title: 'Это название 3', body: 'Это описание 3'},
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost(newPost) {
      this.posts.push(newPost)
    }
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-size: 16px;
  font-family: sans-serif;
}

.app {
  margin: 15px;
}
</style>
