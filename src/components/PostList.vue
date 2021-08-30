<template>
<div>
  <h3>Срисок пользователей</h3>
  <post-item
    v-for="post in posts" 
    :post="post"
    :key="post.id"
  />
</div>
</template>

<script>
import PostItem from "@/components/PostItem.vue";

export default {
  name: 'PostList',
  components: {PostItem},
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
