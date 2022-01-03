<template>

<div>
    <button @click="addLike">Like</button>
    <button @click="addDislike">Dislike</button>

    <div>Количество лайков <strong>{{ likes }}</strong></div>
    <div>Количество дизлайков <strong>{{ dislike }}</strong></div>
</div>

</template>
<script>
export default {
    setup() {
        
    },
}
</script>
<style scoped>

</style>