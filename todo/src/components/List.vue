<template>
<div>
  <div v-bind:key="todo.id" v-for="todo in todos">
    <h1>{{todo.title}} </h1>
   <TodoItem v-bind:todo="todo" />
    
  </div>
  </div>
</template>
<script>

import TodoItem from './TodoItem.vue'


export default {
  name: 'List',
  props: ["todos"],
  components: {
        TodoItem
    }
}
</script>