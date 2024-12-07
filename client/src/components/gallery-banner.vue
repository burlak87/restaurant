<script setup>
    const objectOfText = {
        titleText: 'special offer',
        text: 'upto 45% off',
        btnText: 'check out'
    };
</script>

<template>
    <section class="gallery-banner">
        <slot></slot>
        <article class="gallery-content">
            <h3 class="h3-font"> {{ objectOfText.titleText }} </h3>
            <span class="p-font"> {{ objectOfText.text }} </span>
            <a :href="0" class="btn"> {{ objectOfText.btnText }} </a>
        </article>
    </section>
</template>

<style scoped lang="scss">
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';
</style>