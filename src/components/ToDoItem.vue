<template>
  <div>
    <input type="checkbox" :id="id" :checked="isDone" />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: "ToDoItem",
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
