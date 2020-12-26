<template>
  <div>
    <h2>My todolist</h2>
    <ul>
      <li v-bind:key="todo.id" v-for="todo in todos">
        <Todo v-bind:todo="todo" v-on:delete-todo="$emit('delete-        todo', todo.id)"/>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  props: [
    "todo"
  ],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed
    }
  }
}
</script>
<style scoped>
  .completed {
    text-decoration: line-through;
  }
</style>