<script setup>
    import UpcomingEventsItem from './upcoming-events-item.vue';

    import { onBeforeUnmount, onMounted, ref } from 'vue';

    const day = ref(0);
    const hour = ref(0);
    const minute = ref(0);
    const second = ref(0);

    function deal() {
        const gapDate = new Date('2024-11-30 00:00:00').getTime() - new Date();

        day.value =  Math.floor(gapDate / (1000 * 60 * 60 * 24)),
        hour.value = Math.floor((gapDate % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)),
        minute.value =  Math.floor((gapDate % (1000 * 60 * 60)) / (1000 * 60)),
        second.value =  Math.floor((gapDate % (1000 * 60)) / (1000));
    }

    let intervalId;

    onMounted(() => {
        deal();
        intervalId = setInterval(deal, 1000);
    });

    onBeforeUnmount(() => {
        clearInterval(intervalId);
    });
    
    function msgOfButton() {
        alert("this block has not been implemented yet");
    };

    const objectOfText = {
        titleTextOne: 'deal of the day',
        titleTextTwo: 'Upcoming Events',
        paragraphText: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Assumenda, sequi officiis fugiat accusamus, possimus expedita est quibusdam corrupti cum, debitis minus repellendus laudantium in vitae quisquam! Minus explicabo aliquid quia!',
        btnTextOne: 'check the deal',
        btnTextTwo: 'view our blog'
    };
</script>

<template>
    <h1 class="heading"><span>deal &</span> Events</h1>
    <section class="deal">
        <article class="deal-content">
            <h3 class="h3-font"> {{ objectOfText.titleTextOne }} </h3>
            <p class="p-font"> {{ objectOfText.paragraphText }} </p>
            <section class="count-down">
                <article class="count-down-box">
                    <h3 :id="day"> {{ day }} </h3>
                    <span class="p-font">day</span>
                </article>
                <article class="count-down-box">
                    <h3 :id="hour"> {{ hour }} </h3>
                    <span class="p-font">hour</span>
                </article>
                <article class="count-down-box">
                    <h3 :id="minute"> {{ minute }} </h3>
                    <span class="p-font">minute</span>
                </article>
                <article class="count-down-box">
                    <h3 :id="second"> {{ second }} </h3>
                    <span class="p-font">second</span>
                </article>
            </section>
            <a :href="0" @click.prevent="msgOfButton" class="btn"> {{ objectOfText.btnTextOne }} </a>
        </article>
    </section>
    <section class="events-container">
        <h4> {{ objectOfText.titleTextTwo }} </h4>
        <article class="events-item-box">
            <UpcomingEventsItem>
                <span>22/10/2024</span>
                <h5 class="p-font">Food Flavour</h5>
                <p class="p-font">Flavour so good you'll try <br/> to eat with your eyes</p>
            </UpcomingEventsItem>
            <UpcomingEventsItem>
                <span>22/10/2024</span>
                <h5 class="p-font">healthy food</h5>
                <p class="p-font">Flavour so good you'll try <br/> to eat with your eyes</p>
            </UpcomingEventsItem>
            <UpcomingEventsItem>
                <span>22/10/2024</span>
                <h5 class="p-font">Recipie</h5>
                <p class="p-font">Flavour so good you'll try <br/> to eat with your eyes</p>
            </UpcomingEventsItem>
        </article>
        <a :href="0" @click.prevent="msgOfButton" class="btn upcoming-events"> {{ objectOfText.btnTextTwo }} </a>
    </section>
</template>

<style scoped lang="scss">
    @import '../assets/styles/deal-events.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';

    .deal {
        background-image: url(../assets/images/food.jpg);
    }
</style>