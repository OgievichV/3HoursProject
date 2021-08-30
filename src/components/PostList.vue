<template>
<div v-if="posts.length > 0">
  <h3>Срисок пользователей</h3>
  <post-item
    v-for="post in posts" 
    :post="post"
    :key="post.id"
    @remove="$emit('remove', post)"
  />
</div>
<h2 v-else style="color: red">
Список пользователей пуст
</h2>
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


</style>
