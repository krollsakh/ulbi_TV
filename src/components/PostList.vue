<template>
<div>
  <h1>Список постов</h1>
    <post-item v-for="post in posts" :post="post" :key="post.id"/>
</div>
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  name: "PostList",
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
</style>
