<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <Todo v-bind:todo="todo" v-on:delete="$emit('delete', todo.id)"></Todo>
        </div>
    </div>
</template>

<script>
import Todo from "./Todo";

export default {
    name: "Todos",
    props: ["todos"],
    components: {
        Todo
    }
}
</script>

<style>

</style>
