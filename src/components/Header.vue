<template>
    <header class="container">
        <nav class="navbar navbar-expand-sm justify-content-center justify-content-sm-between">
            <a href="#" class="navbar-brand display-1"><slot></slot></a>
        </nav>
    </header>
</template>

<style scoped lang="scss">
a {
    color: $dark_1;
    font: {
        family: $pixel-font;
        size: 1.5rem;
    }
}
</style>