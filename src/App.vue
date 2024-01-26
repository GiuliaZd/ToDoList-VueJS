<template>
  <div id="app">
    <h1>To-do List</h1>
    <ToDoForm />
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
        <ToDoItem :label="item.label" :done="item.done" :id="item.id" />
      </li>
    </ul>
  </div>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";
import ToDoForm from "./components/ToDoForm.vue";
import uniqueId from "lodash.uniqueid";
export default {
  name: "App",
  components: { ToDoItem, ToDoForm },
  data() {
    return {
      ToDoItems: [
        { id: uniqueId("todo-"), label: "Study VueJS", done: false },
        { id: uniqueId("todo-"), label: "Study Javascript", done: false },
        { id: uniqueId("todo-"), label: "Pass all the exams", done: true },
        {
          id: uniqueId("todo-"),
          label: "Improve your coding skills",
          done: true,
        },
        {
          id: uniqueId("todo-"),
          label: "Learn Typescript and React",
          done: false,
        },
        { id: uniqueId("todo-"), label: "Make the project", done: false },
      ],
    };
  },
};
</script>

<style></style>
