<template>
    <section class="mt-4">
        <input @keydown.enter="AddTodo($event.target.value)" placeholder="Nedir?" type="text"
               class="w-full p-2 bg-gray-700 border-[1px] border-gray-400 rounded-md outline-none">
    </section>
</template>
<script>
export default {
    props: {
        AddTodo: Function,
    }
}
</script>
