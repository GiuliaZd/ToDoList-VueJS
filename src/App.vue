<template>
  <div id="app">
    <h1>To-do List</h1>
    <ToDoItem />
  </div>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";
export default {
  name: "App",
  components: { ToDoItem },
};
</script>

<style></style>
