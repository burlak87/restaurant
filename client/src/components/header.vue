<script setup>
    import { ref } from 'vue';

    const isSearchForm = ref(false);
    const isCartItem = ref(false);

    function searchFormOpen() {
        isSearchForm.value = !isSearchForm.value;
    }

    function cartItemOpen() {
        isCartItem.value = !isCartItem.value;
    }
</script>

<template>
    <header class="header">
        <a href="#" class="logo">
            <img src="../assets/images/logo.png" alt="#">
        </a>
        <nav class="navbar">
            <a href="#home" class="a-font">home</a>
            <a href="#about" class="a-font">about</a>
            <a href="#menu" class="a-font">menu</a>
            <a href="#reservation" class="a-font">reservation</a>
            <a href="#blogs" class="a-font">blogs</a>
            <a href="#review" class="a-font">review</a>
            <a href="#contact" class="a-font">contact</a>
        </nav>
        <article class="icons">
            <section class="fas fa-lightbulb icons-font"></section>
            <section class="fas fa-search icons-font" @click.prevent="searchFormOpen()"></section>
            <section class="fas fa-shopping-cart icons-font" @click.prevent="cartItemOpen()"></section>
            <section class="fas fa-bars icons-font" id="menu-btn"></section>
        </article>
        <article class="search-form" :class="{ active: isSearchForm }">
            <input class="input-font" type="search" id="search-box" placeholder="search here...">
            <label for="search-box" class="fas fa-search icons-font"></label>
        </article>
        <article class="cart-items-container" :class="{ active: isCartItem }">
            <section class="cart-item">
                <span class="fas fa-times icons-font"></span>
                <img src="../assets/images/cart-item-1.jpg" alt="">
                <article class="cart-content">
                    <h3 class="h3-basket-font">cart item</h3>
                    <section class="cart-price price-font">$15.99/</section>
                </article>
            </section>
            <section class="cart-item">
                <span class="fas fa-times icons-font"></span>
                <img src="../assets/images/cart-item-1.jpg" alt="">
                <article class="cart-content">
                    <h3 class="h3-basket-font">cart item</h3>
                    <section class="cart-price price-font">$15.99/</section>
                </article>
            </section>
            <section class="cart-item">
                <span class="fas fa-times icons-font"></span>
                <img src="../assets/images/cart-item-1.jpg" alt="">
                <article class="cart-content">
                    <h3 class="h3-basket-font">cart item</h3>
                    <section class="cart-price price-font">$15.99/</section>
                </article>
            </section>
            <section class="cart-item">
                <span class="fas fa-times icons-font"></span>
                <img src="../assets/images/cart-item-1.jpg" alt="">
                <article class="cart-content">
                    <h3 class="h3-basket-font">cart item</h3>
                    <section class="cart-price price-font">$15.99/</section>
                </article>
            </section>
            <a href="#" class="btn" @click.prevent="msgOfButton">checkout now</a>
        </article>
    </header>
</template>

<style scoped lang="scss">
    @import '../assets/styles/header.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';
</style>