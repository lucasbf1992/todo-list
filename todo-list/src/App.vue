<template>
  <div id="app">     
    <div class="container">
      <am-navbar :titleNavbar="'Lista de Tarefas 1.0'"></am-navbar>
      <am-todo></am-todo>
    </div>      
  </div>
</template>

<script>
import AmTodo from './components/AmTodo.vue';
import AmNavbar from './components/AmNavbar.vue';

export default {
  name: 'App',
  components: {    
    AmNavbar,
    AmTodo
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
