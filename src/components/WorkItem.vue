<script setup lang="ts">
const { work } = defineProps(['work'])

/*
 <div class="col-12 p-0 col-md-4 d-flex flex-column">
        <img :src="work.cover" :alt="work.title + ' cover'" class="img-fluid w-100">
        <h3>{{ work.title }}</h3>
        <p>{{ work.description }}</p>
        <a :href="work.url" class="btn btn-primary-outline">View</a>
    </div>
*/
</script>

<template>
    <div class="col-12 col-md-4 card border-dark p-0">
        <img :src="work.cover" class="card-img-top w-100 img-fluid" :alt="work.title + ' cover'">
        <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p>
            <a :href="work.url" class="btn btn-primary">View</a>
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