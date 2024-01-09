<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Button_Blok from './components/Button_Blok.vue';
import Logo_Blok from './components/Logo_Blok.vue';
import Box_Blok from './components/Box_Blok.vue';
</script>

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
  <Button_Blok bgColor="indigo" buttonText="hello world" boxshadow="5px 2px 2px black" borderRadius="10px" fontSize="50px" textColor="white"/>
  <Logo_Blok src="src\assets\autofleet.png" alt="autofleet logo" width="50%" height="auto"/>
  <Box_Blok display="flex" alignItems="center" justifyContent="center" bgColor="red" content="vasi ca fait chier">
    
  </Box_Blok>
</template>

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
