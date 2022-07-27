<template class="d-flex justify-content-center">
  <img
    alt="ToDoer logo"
    class="rounded header-image"
    src="./assets/logo.png"
    width="128"
    height="128"
  />
  <div class="row d-flex justify-content-between">
    <h1 class="m-auto">ToDoer</h1>
  </div>
  <div id="todo-list" class="col container justify-content-center">
    <ToDoItem text="Do this thing"></ToDoItem>
    <ToDoItem text="Do this other thing"></ToDoItem>
    <ToDoItem text="Do this last thing"></ToDoItem>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ToDoItem from "@/components/ToDoItem.vue";

export default defineComponent({
  name: "App",
  components: { ToDoItem },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
