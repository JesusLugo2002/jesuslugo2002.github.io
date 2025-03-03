<script setup lang="ts">
const { work } = defineProps(['work'])
</script>

<template>
    <a class="col-12 p-0 col-md-4 d-flex flex-column" :href="work.url" target="_blank">
        <div class="w-100 image"></div>
        <h3 class="flex-grow-1">{{ work.title }}</h3>
    </a>
</template>

<style scoped lang="scss">
a {
    color: $white;
    .image {
        height: 200px;
        background-color: $white;
    }
    h3 {
        font-family: $pixel-font;
        background-color: $gray;
    }
}
</style>