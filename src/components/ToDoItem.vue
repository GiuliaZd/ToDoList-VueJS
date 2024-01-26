<template>
  <div>
    <input type="checkbox" id="todo-item" v-bind:checkedSS="isDone" />
    <label for="todo-item">{{ label }}</label>
  </div>
</template>

<script>
export default {
  props: {
    label: { required: true, type: String },
    done: { default: false, type: Boolean },
  },
  data() {
    return {
      isDone: this.done,
    };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
