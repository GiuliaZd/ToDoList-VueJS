<template>
  <form>
    <label for="new-todo-input">What should be done?</label>
    <input type="text" id="new-todo-input" name="to-do" autocomplete="off" />
    <button type="submit">Add new task</button>
  </form>
</template>

<script>
export default { name: "ToDoForm" };
</script>

<style></style>
