<script setup lang="ts">
interface Props {
    name: string
}
defineProps<Props>()
</script>

<template>
    <div class="btn">{{ name }}</div>
</template>

<style scoped>
    .btn {
        border: 1px solid aliceblue;
        border-radius: 20%;
        cursor: pointer;
        padding: 15px;
        display: inline-block;
        margin: 0 10px;
        color: aliceblue;
        font-size: medium;
        font-family: "ff-tisa-web-pro-1", "ff-tisa-web-pro-2", "Lucida Grande", "Hiragino Sans GB", "Hiragino Sans GB W3", "Microsoft YaHei", "WenQuanYi Micro Hei", sans-serif;
        transition: all .3s;
    }

    .btn:hover {
        background-color: aliceblue;
        color: #9a9a9a;
    }
</style>