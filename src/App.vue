<template>
  <div id="app">
    <Todos :todos="list" />
  </div>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      list: [
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
          completed: true
        }
      ]
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
