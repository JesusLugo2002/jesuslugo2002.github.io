<script setup lang="ts">
import { ref } from 'vue';

const email = ref('jesusdlugo02@gmail.com')
const emailCopied = ref(false)

function copyEmail() {
    emailCopied.value = true
    const storage = document.createElement('textarea');
    storage.value = email.value;
    storage.select()
    storage.setSelectionRange(0, 99999)
    navigator.clipboard.writeText(storage.value)
    setTimeout(() => {
        emailCopied.value = false
    }, 3000)
}
</script>

<template>
    <div class="container-fluid bg-dark py-5">
        <div class="container">
            <div class="row">
                <div class="col-sm-6">
                    <p class="text-white h2">Hi! I'm <b>Jesús Lugo</b>, a videogame developer, and I create, develop, design and write.</p>
                    <p class="text-white h5 pt-4">If you have any questions or just want to say hi, feel free to send me a message :)</p>
                    <p class="text-white" v-if="!emailCopied">>> <span class="text-decoration-underline" @click="copyEmail">{{ email }}</span></p>
                    <p class="text-white" v-else>>> Email copied!</p>
                </div>
                <div class="col-sm-6 d-none d-sm-block">
                    <p class="text-white">Image</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
span {
    cursor: pointer;
}
</style>