<template>
  <div class="card todo-item m-5">
    <a v-on:click="check()">
      <div class="card-body">
        <h5 class="card-title">{{ text }}</h5>
        <p class="card-text">{{ description }}</p>
      </div>
    </a>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ToDoItem",
  data: () => ({
    checked: false,
  }),

  props: {
    text: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: false,
      default: "- No description -",
    },
    deadline: {
      type: String,
      required: false,
    },
  },

  methods: {
    check() {
      // Remove todo
      this.checked = true;
      console.log("clicked");
    },
  },
});
</script>

<style scoped lang="scss">
.todo-item {
  offset-position: 20px 20px;
  box-shadow: 2px 2px 2px 1px dimgray;
}

.todo-item:hover {
  opacity: 0.5;
  box-shadow: 0 0 0 0;
}

@import "~bootstrap/dist/css/bootstrap.css";
</style>
