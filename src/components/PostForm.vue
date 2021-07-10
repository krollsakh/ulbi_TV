<template>
  <form @submit.prevent>
    <input class="input" type="text" placeholder="Наименование" v-model="post.title">
    <input class="input" type="text" placeholder="Описание" v-model="post.body">
    <button class="btn" @click="createPost">Добавить пост</button>
  </form>
</template>

<script>
export default {
  name: "PostForm",
  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now()
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: '',
      }
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}

.btn {
  margin-top: 10px;
  align-self: flex-end;
  padding: 10px;
  background: none;
  border: 1px solid #0279F0FF;
}

.input {
  width: 100%;
  margin-top: 10px;
  padding: 10px;
  border: 1px solid #0279F0FF;
}

</style>
