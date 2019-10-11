<template>
  <div id="app">
    <Header />
    <Todos :todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todos from './components/Todos';
import Header from './components/layout/Header';

export default {
  name: 'app',
  components: {
    Header,
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Practice code",
          completed: false
        },
        {
          id: 2,
          title: "Buy groceries",
          completed: false
        },
        {
          id: 3,
          title: "Go for a run",
          completed: false
        }
      ]
    }
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id)
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
