<script setup>
    import { ref } from 'vue' 

    const objectOfText = ref({
        titleText: 'fresh coffee in the morning',
        paragraohText: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed consequuntur natus tempore beatae ipsam culpa praesentium, cumque omnis quisquam a quae in distinctio harum necessitatibus totam saepe odit similique deserunt.',
        btnText: 'get yours now'
    })

    const objectOfAttrs = {
  		id: 'home',
  		class: 'home',
	}

    function msgOfButton() {
        alert("this block has not been implemented yet");
    };
</script>

<template>
    <article v-bind="objectOfAttrs">
        <section class="home-content">
            <h3 class="h3-font"> {{ objectOfText.titleText }} </h3>
            <p class="p-font"> {{ objectOfText.paragraohText }} </p>
            <a :href="0" @click.prevent="msgOfButton" class="btn"> {{ objectOfText.btnText }} </a>
        </section>
    </article>
</template>

<style scoped lang="scss">  
    @import '../assets/styles/home.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';

    .home {
        background-image: url(../assets/images/foto-1.jpg);
    }
</style>