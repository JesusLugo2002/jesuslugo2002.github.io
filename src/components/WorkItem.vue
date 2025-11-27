<script setup lang="ts">
const { work } = defineProps(['work'])
</script>

<template>
    <div class="col-12 col-md-4 card border-dark p-0">
        <img :src="work.cover" class="card-img-top w-100 img-fluid" :alt="work.title + ' cover'">
        <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p>
        </div>
        <div class="btn-group card-footer border-0">
            <a v-if="work.github" :href="work.github" class="btn btn-outline-dark text-center">
                <i class="bi bi-github"></i> Source
            </a>
            <a v-if="work.docs" :href="work.docs" class="btn btn-outline-primary text-center">
                <i class="bi bi-book"></i> Documentation
            </a>
            <a v-if="work.url" :href="work.url" class="btn btn-outline-success text-center">
                <i class="bi bi-globe-americas"></i> Website
            </a>
        </div>
    </div>
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