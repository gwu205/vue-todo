<template>
    <div class="todo-item" :class="{'is-complete':todo.completed}">  
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}}
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: [
        "todo"
    ],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>
    .is-complete {
        text-decoration: line-through;
    }
</style>