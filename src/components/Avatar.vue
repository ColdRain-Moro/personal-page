<script setup lang="ts">
interface Props {
    center: boolean
    src: string
}
const props = withDefaults(defineProps<Props>(), {
    center: true,
})
</script>

<template>
    <div class="avatar-box" :class="{ 'center': center }">
        <img :src="src" alt="img" />
    </div>
</template>

<style scoped>
.avatar-box {
    display: flex;
    justify-self: center;
    align-self: center;
    flex-direction: row;
    border-radius: 100%;
    width: 120px;
    height: 120px;
    transition: all .8s;
}

.center {
    margin: auto;
}

img {
    width: 100%;
    height: 100%;
    border-radius: 100%;
}

@media (max-width: 780px) {
    .avatar-box {
        width: 100px;
        height: 100px;
    }
}

.avatar-box:hover {
    width: 150px;
    height: 150px;
}

</style>