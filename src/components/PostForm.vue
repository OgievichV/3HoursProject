<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
      v-model="post.title"
      type="text"
      placeholder="Название"
    />
    <input
      v-model="post.body"
      type="text"
      placeholder="Описание"
    />
    <button
      style="align-self: flex-end; margin-top: 15px"
      @click="createPost"
    >
      Создать
    </button>
  </form>
</template>

<script>
export default {
  name: 'PostList',
  components: {},
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: ''
      }
    }
  },
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
</style>