<template>
  <div>
    <input type="checkbox" id="todo-item" v-bind:checkedSS="isDone" />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
import uniqueId from "lodash.uniqueid";
export default {
  props: {
    label: { required: true, type: String },
    done: { default: false, type: Boolean },
  },
  data() {
    return {
      isDone: this.done,
      id: uniqueId("todo-"),
    };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
