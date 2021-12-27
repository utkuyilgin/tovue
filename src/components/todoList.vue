<template>
    <section class="mt-4">
        <TodoListItem v-for="todoItem in todoList" :key="todoItem.id" :todo="todoItem"/>
        <small>{{ todoLength }} item vardır.</small>
        <div class="text-green-400">Tamamlananlar</div>
        <div class="text-red-400">Tamamlanmayanlar</div>
    </section>
</template>
<script>
import TodoListItem from './TodoListItem.vue';
import {computed} from "vue";

export default {
    components: {
        TodoListItem,
    },
    props: {
        todoList: Array,
        utku: String
    },
    setup(props) {
        const todoLength = computed(() => props.todoList.length);
        return {todoLength}
    }
};
</script>
