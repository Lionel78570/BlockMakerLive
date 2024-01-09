<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    buttonText: String,
    bgColor: String,
    boxshadow: String,
    textColor: String,
    borderRadius: String,
    fontSize: String,
    padding: String,
});

const handleClick = () => {
    // Logique à exécuter lors du clic sur le bouton
};
</script>

<template>
    <button class="btn" @click="handleClick" :style="{ backgroundColor: bgColor, boxShadow: boxshadow ,borderRadius: borderRadius,fontSize: fontSize,color: textColor}">
        {{ buttonText }}
    </button>
</template>

<style scoped>
.btn {
    border: none;
    color: #fff;
    padding: 0.5em 1em;
    transition: background-color 0.3s ease;
    cursor: pointer;
}
</style>
