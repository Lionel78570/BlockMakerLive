<template>
    <button class="btn" @click="handleClick">{{ buttonText }}</button>
</template>

<script>
export default {
    data() {
        return {
            buttonText: "Cliquez ici"
        };
    },
    methods: {
        handleClick() {
            // Logique à exécuter lors du clic sur le bouton
        }
    }
};
</script>

<style scoped>
.btn {
    /* Styles pour le bouton */
}
</style>
