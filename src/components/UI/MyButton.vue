<template>
  <button class="btn">
      <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'my-button',
  components: {},
  props: {},
  data() {
    return {}
  },
  mounted() {},
  beforeDestroy() {},
  methods: {}
}
</script>

<style lang="css" scoped>
.btn {
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>
