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
    <div id="works-container" class="container-fluid pt-1">
        <h2>My portfolio</h2>
        <div class="row">
            <WorkItem v-for="work in selectedWork" :work="work"/>
        </div>
    </div>
</template>

<style scoped lang="scss">
#works-container {
    background-color: $dark_1;
    color: $white;
    h2 {
        font-family: $pixel-font;
    }
}
</style>