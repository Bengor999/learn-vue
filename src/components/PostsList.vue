<template>

    <div class="post" v-for="post in posts">
        <div><strong>Название:</strong>{{post.title}}</div>
        <div><strong>Описание:</strong>{{post.body}}</div>

    </div>

</template>
<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true,
        }

    },
    setup() {
        
    },
}
</script>
<style scoped>
.post {
    padding: 15px;
    border: 2px solid greenyellow;
    width: 1300px;
    margin: 0 auto;
}

</style>
