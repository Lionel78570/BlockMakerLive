
<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
  <DropDown_Blok :label="'Menu BURGER'" :options="dropDownOptions" :selectedOption="selectedOption" @update:selectedOption="selectedOption = $event" />

</template>

<script>
import DropDown_Blok from '../src/components/DropDown_Blok.vue';
export default {
  components: {
    DropDown_Blok
  },
  data() {
    return {
      dropDownOptions: ['MENU 1', 'MENU 2', 'MENU 3'],
      selectedOption: 'MENU 2'
    };
  }
};
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>