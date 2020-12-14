<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to your Todo List (made with Vue)"/>
    <Todos v-bind:todos="todos"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Todos
  },
  data(){
  return {
    todos: [
      {
      id:1,
      title: 'Workout',
      completed: false
      },
      {
      id:1,
      title: 'Eat ',
      completed: false
      },
      {
      id:1,
      title: 'Take shower',
      completed: false
      }
    ]
  }}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
