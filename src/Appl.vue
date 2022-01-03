<template>
<div>
    <like/>
    <post-form/>
    <posts-list :posts="posts" />
</div>
</template>
<script>
import PostForm from "./components/PostForm";
import Like from './components/Like';
import PostsList from './components/PostsList';

export default {
    components: {
        PostForm,
        Like,
        PostsList
    },
    data() {
        return {
            posts:[
                {id: 1, title: 'JavaSkript', body: 'Описание поста'},
                {id: 2, title: 'JavaSkript 2 ', body: '66666666Описание поста'},
                {id: 3, title: 'JavaSkript 3 33', body: 'Описан55555555ие поста'},
            ],
            title: '',
            body: '',
            likes: 0,
            dislike: 0,
        }
    },
    methods: {
        createPost (){
            const newPost = {
                id: Date.now(),
                title: this.title,
                body: this.body,
            }
            this.posts.push(newPost);
            this.title = '';
            this.body = '';
        },
        addLike() {
            this.likes += 1;
        },
        addDislike() {
            this.dislike += 1;
        }
    }


}
</script>
<style>
* {
    margin: 0;
    padding: 0;
    border: 0;
    box-sizing: border-box;
}
button {
    padding: 10px 20px;
    background-color: aqua;
    margin: 20px;
    border-radius: 10px;
}
input {
    background-color: goldenrod;
    border: hotpink 1px solid;
    padding: 5px 10px;
    margin: 20px;
}

</style>