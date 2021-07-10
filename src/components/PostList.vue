<template>
<div>
  <h1>Список постов</h1>
</div>
</template>

<script>
export default {
  name: "PostList",
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid #0279F0FF;
  margin-top: 15px;
}
</style>
