<template>
  <input :value="modelValue" @input="updateInput" class="input" type="text">
</template>

<script>
export default {
  name: 'my-input',
  components: {},
  props: {
    modelValue: [String, Number]
  },
  data() {
    return {}
  },
  mounted() {},
  beforeDestroy() {},
  methods: {
    updateInput(event) {
      this.$emit('update:madelValue', event.target.value)
    }
  }
}
</script>

<style lang="css" scoped>
.input {
  width: 100%;
  border: 1px solid teal; 
  padding: 10px 15px;
  margin-top: 15px;
}
</style>
