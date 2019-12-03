<template>
  <div v-bind:class="{'is-complete':todo.completed}">
        <!-- <p>
          <input type="checkbox" v-on:change="markComplete" >
          Todo items
          <button @click="$emit('del-todo', todo.id)" class="del">x</button>
        </p> -->
        <h1>{{todo.title}}</h1>
      
      </div>
</template>

<script>


export default {
    name: "TodoItem",
    props: ["todos"],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>
.is-completed {
    text-decoration: line-through;
}
</style>