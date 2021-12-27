<template>
    <div class="w-screen h-screen bg-gray-400 pt-10">
        <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3 mt-10">
            <h3 class="text-center text-2xl">TodoList</h3>
            <AddSection :AddTodo="AddTodo"/>
            <TodoList :todoList="todoList" utku="zeynep"/>
        </div>
    </div>
</template>
<script>
import AddSection from "./components/addSection.vue";
import TodoList from "./components/todoList.vue";
import { ref } from "vue"

export default {
    components: {
        AddSection,
        TodoList,
    },
    setup() {
        const todoList = ref([]);
        const AddTodo = (todoText) => {
            todoList.value.push({
                id: new Date().getTime(),
                title: todoText,
            })
        }
        return {todoList, AddTodo};
    }
};
</script>
