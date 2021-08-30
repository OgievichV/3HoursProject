<template>
  <div class="post">
      <div>
        <div><strong>Название:</strong> {{post.title}}</div>
        <div><strong>Описание:</strong> {{post.body}}</div>
      </div>
      <div class="post__btns"> 
        <my-button 
          @click="$emit('remove', post)"
        >
          Удалить
        </my-button>
      </div>
  </div>
</template>

<script>

export default {
  name: 'PostItem',
  components: {},
  props: {
    post: {
      type: Object,
      required: true,
    }
  },
  data() {
    return {}
  },
  mounted() {},
  beforeDestroy() {},
  methods: {}
}
</script>

<style lang="css" scoped>
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
    display: flex;
    justify-content: space-between;
}

</style>
