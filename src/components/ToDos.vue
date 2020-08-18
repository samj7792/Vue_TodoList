<template>
  <div>
    <!-- todo in v-for can be whatever, todos pertains to the prop -->
    <div v-bind:key="todo.id" v-for="todo in todos">
      <ToDoItem v-bind:todo="todo" @del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script>
import ToDoItem from "./ToDoItem";

export default {
  name: "Todos",
  components: { ToDoItem },
  props: ["todos"],
};
</script>

<style scoped>
</style>