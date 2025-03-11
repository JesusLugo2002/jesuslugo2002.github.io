<script setup lang="ts">
const { work } = defineProps(['work'])
</script>

<template>
    <a class="col-12 p-0 col-md-4 d-flex flex-column" :href="work.url" target="_blank">
        <img :src="work.cover" :alt="work.title + ' cover'" class="img-fluid w-100">
        <h3 class="flex-grow-1">{{ work.title }}</h3>
    </a>
</template>

<style scoped lang="scss">
a {
    color: $dark_1;
    img {
        height: 200px;
        background-image: none;
    }
    h3 {
        font-family: $pixel-font;
        background-color: $light_gray;
    }
}
</style>