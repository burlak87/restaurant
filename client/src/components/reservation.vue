<script setup>
    const objectOfText = {
        titleText: 'Reservation',
        titleTextTwo: 'Take a Reservation',
        titleTextThree: 'MARK WILLY',
        text: 'Head Shef',
        paragraphText: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto, odio accusamus unde consequatur vero omnis nihil a maiores?',
        btnText: 'Book A Table'
    }

    function onSubmitForm() {
        alert("You have successfully taken a place!");
    };
</script>

<template>
    <h1 class="heading"> {{ objectOfText.titleText }} </h1>
    <article id="reservation" class="reservation">
        <form class="input-form-box">
            <h3 class="h3-font"> {{ objectOfText.titleTextTwo }} </h3>
            <input class="input-font" type="text" placeholder="Name">
            <input class="input-font" type="email" placeholder="Email">
            <input class="input-font" type="number" placeholder="Phone">
            <input class="input-font" type="date">
            <input class="input-font" type="time">
            <input class="input-font" type="text" placeholder="Massage">
            <a :href="0" class="btn" @submit.prevent="onSubmitForm"> {{ objectOfText.btnText }} </a>
        </form>
        <section class="reservation-content">
            <h3 class="h3-font"> {{ objectOfText.titleTextThree }} </h3>
            <span class="p-font"> {{ objectOfText.text }} </span>
            <p class="p-font"> {{ objectOfText.paragraphText }} </p>
        </section>
    </article>
</template>

<style scoped lang="scss">
    @import '../assets/styles/reservation.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';
</style>