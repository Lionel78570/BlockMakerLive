<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    src: String,
    alt: String,
    width: {
        type: [String, Number],
        default: '100%',
    },
    height: {
        type: [String, Number],
        default: 'auto',
    },
});
const handleClicklogo = () => {
    // Logique à exécuter lors du clic sur le bouton
};
</script>

<template>
    <img class="logo" @click="handleClicklogo"  :src="src" :alt="alt" :width="width" :height="height" />
</template>


<style scoped>
</style>