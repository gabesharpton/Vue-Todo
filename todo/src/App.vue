<template>
  <div id="app">
    
    <HelloWorld msg="To Do List"/>
    <List msg="Todo"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import List from './components/List.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    List
  },
  data() {
    todos: [
      {
        id:1,
        title:"Todo One",
        completed: false
      },
      {
        id:2,
        title:"Todo two",
        completed: false
      },
      {
        id:3,
        title:"Todo three",
        completed: false
      }
    ]
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
