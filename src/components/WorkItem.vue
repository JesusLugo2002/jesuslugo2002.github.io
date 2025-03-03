<script setup lang="ts">
const { work } = defineProps(['work'])
</script>

<template>
    <a class="col-12 p-0 col-md-4 d-flex flex-column text-white text-decoration-none" :href="work.url" target="_blank">
        <div class="placeholder w-100"></div>
        <h3 class="flex-grow-1">{{ work.title }}</h3>
    </a>
</template>

<style scoped>
h3 {
    font-family: "Pixelify Sans", serif;
    background-color: rgb(97, 94, 94);
}
.placeholder {
    height: 200px;
}
</style>