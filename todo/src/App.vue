<template>
  <div id="app">
    
    <HelloWorld msg="To Do List"/>
    
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    Todos
  },
  data() {
    return {
      todos: [
        {
          id:1,
          title:"Todo One",
          completed: false
        },
        {
          id:2,
          title:"Todo Two",
          completed: true
        },
        {
          id:3,
          title:"Todo Three",
          completed: false
        }
    ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
