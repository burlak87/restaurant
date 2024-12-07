<script setup>
    const titleText = 'get in touch';
    const contactNow = 'contact now';

    function onSubmitForm() {
        alert("you will be contacted soon");
    };
</script>

<template>
    <article class="contact" id="contact">
        <h1 class="heading"><span>contact</span> us</h1>
        <section class="contact-row">
            <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d33315.16922475341!2d31.261459000000002!3d58.541697!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46beebb1dffe1b91%3A0xc8540dcd83cfa2e4!2z0J3QvtCy0LPQvtGA0L7QtNGB0LrQuNC5INCz0L7RgdGD0LTQsNGA0YHRgtCy0LXQvdC90YvQuSDRg9C90LjQstC10YDRgdC40YLQtdGCINC40LzQtdC90Lgg0K_RgNC-0YHQu9Cw0LLQsCDQnNGD0LTRgNC-0LPQvg!5e0!3m2!1sru!2sru!4v1724782923999!5m2!1sru!2sru" allowfullscreen="" loading="lazy"></iframe>            
            <form action="">
                <h3 class="h3-font"> {{ titleText }} </h3>
                <section class="contact-inputBox">
                    <span class="fas fa-user icons-font"></span>
                    <input class="input-font" type="text" placeholder="name">
                </section>
                <section class="contact-inputBox">
                    <span class="fas fa-envelope icons-font"></span>
                    <input class="input-font" type="email" placeholder="email">
                </section>
                <section class="contact-inputBox">
                    <span class="fas fa-phone icons-font"></span>
                    <input class="input-font" type="number" placeholder="number">
                </section>
                <a :href="0" class="btn" type="submit" @submit.prevent="onSubmitForm"> {{ contactNow }} </a>
            </form>
        </section>
    </article>
</template>

<style scoped lang="scss">
    @import '../assets/styles/contact-us.scss';
    @import '../assets/styles/button.scss';
</style>