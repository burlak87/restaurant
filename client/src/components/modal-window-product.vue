<script setup>
    import { defineProps, defineEmits } from 'vue';
    
    const emit = defineEmits(['close']);
    
    const props = defineProps({
        isOpen: {
            type: Boolean,
            default: true
        },
        titleName: String,
        paragraph: String,
        spanText: String
    })

    const close = () => {
        emit('close');
    };

</script>

<template>
    <article>
        <section>
            <h2> {{ titleName }} </h2>
            <p> {{ paragraph }} </p>
            <span> {{ spanText }} </span>
            <article>
                <button @click.prevent="close">закрыть</button>
                <button>добавить в корзину</button>
            </article>
        </section>
    </article>
</template>

<style scoped lang="scss">

</style>