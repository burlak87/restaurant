<script setup>
    function msgOfButton() {
        alert("this block has not been implemented yet");
    };
</script>

<template>
    <article class="blogs" :id="blogs">
        <h1 class="heading">our <span>blogs</span></h1>
        <section class="blogs-container">
            <article class="blogs-box">
                <section class="blogs-image">
                    <img src="../assets/images/foto-6.jpg" alt="">
                </section>
                <section class="blogs-content">
                    <a :href="0" @click.prevent="msgOfButton" class="title h3-font">tasty and refreshing coffee</a>
                    <span class="p-font">by admin / 21st may, 2021</span>
                    <p class="p-font">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis harum consequuntur corporis quis, laboriosam, quisquam laudantium ipsum dolore quidem animi adipisci nemo, suscipit modi dolor ab incidunt distinctio excepturi illo!</p>
                    <a :href="0" @click.prevent="msgOfButton" class="btn">read more</a>
                </section>
            </article>
            <article class="blogs-box">
                <section class="blogs-image">
                    <img src="../assets/images/foto-6.jpg" alt="">
                </section>
                <section class="blogs-content">
                    <a :href="0" @click.prevent="msgOfButton" class="title h3-font">tasty and refreshing coffee</a>
                    <span class="p-font">by admin / 21st may, 2021</span>
                    <p class="p-font">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis harum consequuntur corporis quis, laboriosam, quisquam laudantium ipsum dolore quidem animi adipisci nemo, suscipit modi dolor ab incidunt distinctio excepturi illo!</p>
                    <a :href="0" @click.prevent="msgOfButton" class="btn">read more</a>
                </section>
            </article>
            <article class="blogs-box">
                <section class="blogs-image">
                    <img src="../assets/images/foto-6.jpg" alt="">
                </section>
                <section class="blogs-content">
                    <a :href="0" @click.prevent="msgOfButton" class="title h3-font">tasty and refreshing coffee</a>
                    <span class="p-font">by admin / 21st may, 2021</span>
                    <p class="p-font">Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis harum consequuntur corporis quis, laboriosam, quisquam laudantium ipsum dolore quidem animi adipisci nemo, suscipit modi dolor ab incidunt distinctio excepturi illo!</p>
                    <a :href="0" @click.prevent="msgOfButton" class="btn">read more</a>
                </section>
            </article>
        </section>
    </article> 
</template>

<style scoped lang="scss">
    @import '../assets/styles/our-blogs.scss';
    @import '../assets/styles/button.scss';
    @import '../assets/styles/fonts.scss';
</style>