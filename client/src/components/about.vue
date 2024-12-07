<script setup>
    import VideoModal from './video-modal.vue';
    import ourStrenghtItem from './our-strenght-item.vue';

    import { ref } from 'vue';

    const showModal = ref(false);

    const openModal = () => {
        showModal.value = true;
    };

    const closeModal = () => {
        showModal.value = false;
    };

    function msgOfButton() {
        alert("this block has not been implemented yet");
    };

    const objectOfText = {
        titleOne: 'Hygienic Food',
        titleTwo: 'Fresh Environment',
        titleThree: 'Skilled Chefs',
        titleFour: 'Event & Party'
    }
</script>

<template>
    <h1 class="heading"><span>about</span> us</h1>
    <section class="about-row">
        <article class="about-image">
            <img src="../assets/images/foto-5.jpg" alt="">
        </article>
        <article class="about-content">
            <h3 class="h3-font">what makes our coffee special?</h3>
            <p class="p-font">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum sequi, aspernatur quia, 
                labore quod fugiat alias temporibus soluta quis natus, voluptatem eaque! Eveniet eum earum, 
                iusto iste laboriosam ex itaque!</p>
            <p class="p-font">Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam culpa maxime tempora 
                dolorum cum architecto repudiandae ut vel inventore, qui temporibus quisquam provident et 
                dicta soluta minima placeat voluptate fugit?</p>
            <a :href="0" @click.prevent="msgOfButton" class="btn">learn more</a>
        </article>
    </section>
    <h1 class="heading"> <span>Discover</span> our <br/> restaurant <span>story</span></h1>
    <section class="about-story">
        <p class="p-font-two">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Deserunt quod dolor, qui quae <br/>
            ipsum exercitationem optio iste autem porro? Animi voluptate in praesentium laboriosam excepturi <br/>
            deserunt soluta amet laborum magnam.</p>
        <button class="play-btn" @click="openModal">
            <i class="fas fa-play icons-font"></i>
        </button>
    </section>
    <VideoModal v-if="showModal" @close="closeModal" />
    <h1 class="heading"><span>our</span> strenght</h1>
    <section class="our-strenght-row">
        <ourStrenghtItem>
            <section class="our-strenght-item-icon">
                <i class="fas fa-hot-tub icons-font"></i>
            </section>
            <h5 class="h5-font"> {{ objectOfText.titleOne }} </h5>
        </ourStrenghtItem>
        <ourStrenghtItem>
            <section class="our-strenght-item-icon">
                <i class="fas fa-air-freshener icons-font"></i>
            </section>
            <h5 class="h5-font"> {{ objectOfText.titleTwo }} </h5>
        </ourStrenghtItem>
        <ourStrenghtItem>
            <section class="our-strenght-item-icon">
                <i class="fas fa-utensils icons-font"></i>
            </section>
            <h5 class="h5-font"> {{ objectOfText.titleThree }} </h5>
        </ourStrenghtItem>
        <ourStrenghtItem>
            <section class="our-strenght-item-icon">
                <i class="fas fa-birthday-cake icons-font"></i>
            </section>
            <h5 class="h5-font"> {{ objectOfText.titleFour }} </h5>
        </ourStrenghtItem>
    </section>
</template>

<style scoped lang="scss">
    @import '../assets/styles/about.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';

    .about-story {
        background-image: url(../assets/images/foto-7.jpg);
    }
</style>