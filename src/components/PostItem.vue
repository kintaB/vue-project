<template>
    <div class="post">
        <div>
            <div>
                Название: <strong> {{ post.title }} </strong> 
            </div>
            <div>
                Описание: <strong> {{ post.description }} </strong> 
            </div>
        </div>
        <div class="post__buttons">
            <VUEButton>Удалить</VUEButton>
        </div>
    </div>
</template>

<script>
import VUEButton from './UI/VUEButton.vue';

    export default {
    props: {
        post: Object,
        required: true
    },
    components: { VUEButton }
}
</script>

<style scoped>
.post {
    margin-top: 10px;
    padding: 15px;
    border: 3px solid teal;
    display: flex;
    align-items: center;
    justify-content: space-between;
    
}
</style>