<template>
    <div class="app">
        <PostForm @create="createPost" />
        <PostList :posts="posts"  />
    </div>

</template>

<script>
import PostForm  from './components/PostForm.vue'
import PostList from './components/PostList.vue'

export default {
    components:{
        PostForm,
        PostList
    },  
    data() {
        return {
            posts: [
                { 
                    id: 1,
                    title: 'Название1', 
                    description: 'Опиcaние1'  
                },
                { 
                    id: 2,
                    title: 'Название2', 
                    description: 'Описание2'  
                },
                { 
                    id: 3,
                    title: 'Название3', 
                    description: 'Описание3'  
                },
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post)
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 16px;
}
</style>