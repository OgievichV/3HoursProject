<template>
  <div 
    class="post" 
    v-for="post in posts" 
    :key="post.id"
  >
    <div><strong>Название:</strong> {{post.title}}</div>
    <div><strong>Описание:</strong> {{post.body}}</div>
    </div>
</template>

<script>
export default {
  name: 'PostList',
  components: {},
  props: {
    posts: {
      type: Array,
      required: true
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
}

</style>
