<script setup>
    import { ref, onMounted } from 'vue';

    const isLoaded = ref(false);

    onMounted(() => {
        setTimeout(() => {
            isLoaded.value = true;
        }, 1500);
    });

    const objectOfAttrs = {
        id: 'preload',
        class: 'preload'
    };
</script>

<template>
    <section v-bind="objectOfAttrs" :class="{ loaded: isLoaded }" data-preaload>
        <article class="circle"></article>
        <p class="preloader-text preloader-font">Restaurant</p>
    </section>
</template>

<style scoped lang="scss">
    @import '../assets/styles/preloader.scss';
    @import '../assets/styles/fonts.scss';
</style>