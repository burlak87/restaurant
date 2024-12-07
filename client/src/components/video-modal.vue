<script setup>
    import { ref, defineProps, defineEmits } from 'vue';

    const emit = defineEmits(['close']);

    const props = defineProps({
        isOpen: {
            type: Boolean,
            default: true
        }
    });

    const close = () => {
        emit('close');
    };
</script>

<template>
    <section v-if="props.isOpen" class="modal-overlay" @click.self="close">
        <article class="modal">
            <button class="close-btn" @click.prevent="close">✖</button>
            <video controls autoplay loop width="800" height="530">
                <source src="../assets/videos/videos-chef.mp4" type="video/mp4" />
                <p class="p-font">Your browser doesn't support HTML5 video. Here is a <a href="">link to the video</a> instead.</p>
            </video>
        </article>
    </section>
</template>

<style scoped lang="scss">
    @import '../assets/styles/video-modal.scss';
    @import '../assets/styles/fonts.scss';
</style>

  