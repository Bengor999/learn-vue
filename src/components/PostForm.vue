<template>

<div>
    <form @submit.prevent>
        <h4>Создание поста</h4>
        <input 
            v-bind:value="post.title" 
            @input="post.title = $event.target.value"
            type="text" 
            placeholder="Название"
        >
        <input  
            v-bind:value="post.body" 
            @input="post.body = $event.target.value"
            type="text" 
            placeholder="Описание"
        >
        <button>Добавить пост</button>
    </form>
</div>

</template>
<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            }
        }
        
    },
}
</script>
<style scoped>

</style>