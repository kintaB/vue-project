<template>
    <form class="form" @submit.prevent>
        <input 
            v-model="post.title"
            class="input-form"
            type="text"
            placeholder="Название"
        >
        <input 
            v-model="post.description"
            class="input-form" 
            type="text" 
            placeholder="Описание">
        <VUEButton @click="createPost">Создать пост</VUEButton>
    </form>
</template>

<script>

export default {
    data() {
        return {
            post: {
                title: "",
                description: "",
            }
        };
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit("create", this.post);
            this.post = {
                title: "",
                description: "",
            };
        }
    }
}
</script>


<style scoped>


.form {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
}

.input-form {
    width: 100%;
    border: 2px solid teal;
    margin-top: 10px;
    height: 80px;
    padding: 10px;
    font-size: medium;
}
</style>