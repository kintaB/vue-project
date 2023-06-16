<template>
    <button class="btn">
    <slot></slot>
    </button>
</template>

<script>
    export default {
        name: 'VUEButton'
    }
</script>

<style scoped>
.btn {
    margin-top: 10px;
    border: none;
    border-radius: 20px;
    font-size: medium;
    padding: 10px;
    background-color: white;
    align-self: flex-end;
    border: 1px solid teal;
}
</style>