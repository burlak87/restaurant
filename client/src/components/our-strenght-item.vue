<script setup>
    const paragraph = 'Lorem ipsum dolor sit, amet consectetur adipisicing elit.';
</script>

<template>
    <article class="our-strenght-item">
        <slot></slot>
        <p class="p-font"> {{ paragraph }} </p>
    </article>
</template>

<style scoped lang="scss">
   p {
    font-size: 1rem;
    text-align: center;
   }
</style>