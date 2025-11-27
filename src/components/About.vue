<script setup lang="ts">
import { onMounted, ref } from 'vue';

const email = ref('jesusdlugo02@gmail.com')
const emailCopied = ref(false)

/**
 * Enable copy email on label click.
 */
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

const actions = ['create.', 'develop.', 'design.', 'write.', 'play.'];
const currentAction = ref("");

/**
 * Create typewriting animation on subtitle.
 */
function writeWord(actionIndex: number) {
    function writeChar(charIndex: number = 0) {
        currentAction.value += actions[actionIndex][charIndex++]
        if (charIndex < actions[actionIndex].length) {
            setTimeout(() => {
                writeChar(charIndex)
            }, 120)
        } else {
            setTimeout(() => {
                currentAction.value = ""
                if (actionIndex < actions.length - 1) {
                    actionIndex++;
                } else {
                    actionIndex = 0;
                }
                writeWord(actionIndex)
            }, 1300)
        }
    }
    writeChar();
}

onMounted(() => {
    writeWord(0)
})
</script>

<template>
    <div id="about-container" class="container-fluid py-5">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <p class="h2">Hi! I'm <b>Jesús Lugo</b>, a videogame developer, and I {{ currentAction }}</p>
                    <p class="h5 pt-4">If you have any questions or just want to say hi, feel free to send me a message :)</p>
                    <p v-if="!emailCopied">>> <a @click="copyEmail">{{ email }}</a></p>
                    <p v-else>>> Email copied!</p>
                </div>
                <div class="col-md-6 d-none d-sm-block">
                    <!-- Dibujo aqui -->
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
#about-container {
    background-color: $dark_2;
    p {
        color: $white;
    }
    b {
        color: $primary;
    }
    a {
        cursor: pointer;
        text-decoration: underline;
    }
}

</style>