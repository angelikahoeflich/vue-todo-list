<template>
  <div>
    <h2>My To Do List</h2>
    <ul>
      <li v-bind:key="todo.id" v-for="todo in todos">
        <Todo v-bind:todo="todo" />
      </li>
    </ul>
  </div>

</template>


<script>
import Todo from './Todo';

export default {
  name:'Todos',
  components: {
    Todo 
    },
    props: [
      "todos"
      ]
    }

</script>

<style scoped></style>