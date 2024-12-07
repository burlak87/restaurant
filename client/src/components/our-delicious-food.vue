<script setup>
    import { onMounted } from 'vue';

    onMounted(() => {
        let swiper = new Swiper(".food-slider", {
            grabCursor: true,
            loop: true,
            centeredSlides: true,
            spaceBetween: 20,
            pagination: {
                el: ".swiper-pagination",
                clickable: true,
            },
            breakpoints: {
                0: {
                    slidesPerView: 1,
                },
                700: {
                    slidesPerView: 2,
                },
                1000: {
                    slidesPerView: 3,
                }
            }
        })
    });
</script>

<template>
    <article class="food">
        <section class="swiper food-slider">
            <h1 class="heading">Our <span>Delicious</span> Food</h1>
            <article class="swiper-wrapper">
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
                <section class="swiper-slide slide" data-name="food-1">
                    <img src="../assets/images/food-slide.png" alt="">
                    <h3 class="h3-font">delicious food</h3>
                    <p class="price-food-slider price-font">$49.99</p>
                </section>
            </article>
            <article class="swiper-pagination"></article>
        </section>
    </article>
</template>

<style scoped lang="scss">
    @import '../assets/styles/our-delicious-food.scss';
    @import '../assets/styles/fonts.scss';
</style>