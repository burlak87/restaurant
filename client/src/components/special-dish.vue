<script setup>
    import GalleryBanner from './gallery-banner.vue';
    import { ref } from 'vue'

    const objectOfText = ref({
        titleText: 'Meat',
        paragraohText: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed consequuntur natus tempore beatae ipsam culpa praesentium, cumque omnis quisquam a quae in distinctio harum necessitatibus totam saepe odit similique deserunt.',
        btnText: 'add to cart',
        oldPriceText: '24.99$',
        newPriceText: '19.99$'
    });

    function msgOfButton() {
        alert("this block has not been implemented yet");
    };
</script>

<template>
    <h1 class="heading"><span>special</span> dish</h1>
    <section class="special-dish-row">
        <article class="special-dish-content">
            <h3 class="h3-font"> {{ objectOfText.titleText }} </h3>
            <p class="p-font"> {{ objectOfText.paragraohText }} </p>
            <section class="price-product-item price-font"> {{ objectOfText.newPriceText }} <span class="price-sale-font"> {{ objectOfText.oldPriceText }} </span></section>
            <a :href="0" @click.prevent="msgOfButton" class="btn"> {{ objectOfText.btnText }} </a>
        </article>
        <article class="special-dish-banner">
            <img src='../assets/images/foto-5.jpg' alt='special-dish'>
        </article>
    </section>
    <article class="banner-box">
        <GalleryBanner>
            <img src="../assets/images/foto-4.jpg" alt="">
        </GalleryBanner>
        <GalleryBanner>
            <img src="../assets/images/foto-3.jpg" alt="">
        </GalleryBanner>
        <GalleryBanner>
            <img src="../assets/images/foto-2.jpg" alt="">
        </GalleryBanner>
    </article>
</template>

<style scoped lang="scss">
    @import '../assets/styles/special-dish.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';
</style>