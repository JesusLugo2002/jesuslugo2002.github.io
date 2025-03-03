<script setup lang="ts">
import { onMounted, ref } from 'vue';
import WorkItem from './WorkItem.vue';

const selectedWork = ref([]);

onMounted(async() => {
    try {
        const response = await fetch('selected-work.json')
        selectedWork.value = await response.json()
    } catch (error) {
        console.error("Something goes wrong fetching works data!", error)
    }
})
</script>

<template>
    <div class="container-fluid bg-dark text-white">
        <h2>Selected work</h2>
        <div class="row">
            <WorkItem v-for="work in selectedWork" :work="work"/>
        </div>
    </div>
</template>

<style scoped>
h2 {
    font-family: "Pixelify Sans", serif;
}
</style>