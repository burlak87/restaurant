<script setup>
    import { ref } from 'vue';
    // import ModalWindowProduct from '../components/modal-window-product.vue';

    const showModal = ref(false);

    const openModal = () => {
        showModal.value = true;
    };

    const closeModal = () => {
        showModal.value = false;
    };

    defineProps({
        imgPath: String,
        title: String,
        text: String,
        spanTxt: String,
        btn: String
    })
</script>

<template>
    <section class="product-item">
        <img class="image-product" :src="imgPath" alt="0">
        <h3 class="h3-basket-font">{{ title }}</h3>
        <article class="price-product-item price-font">{{ text }} <span class="price-sale-font">{{ spanTxt }}</span></article>
        <a href="#" class="btn" @click.prevent="openModal">{{ btn }}</a>
    </section>
    <ModalWindowProduct v-if="showModal" @close="closeModal" />
</template>

<style scoped lang="scss">
    @import "../assets/styles/product-item.scss";
    @import "../assets/styles/button.scss";
    @import '../assets/styles/fonts.scss';
</style>