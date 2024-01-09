<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    content: String,
    display: String,
    alignItems: String,
    justifyContent: String,
    bgColor: String,
});

</script>

<template>
    <div  :style="{ backgroundColor: bgColor, display: display, justifyContent: justifyContent, alignItems: alignItems}">
    {{ content }}</div>
</template>


<style scoped>
</style>