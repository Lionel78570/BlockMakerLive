<template>
  <nav>
    <ul>
      <li v-for="link in links" :key="link.path">
        <router-link :to="link.path">{{ link.text }}</router-link>
        <DropDown_Blok v-if="link.submenu" :links="link.submenu" />
      </li>
    </ul>
  </nav>
</template>

<script>
import DropDown_Blok from './DropDown_Blok.vue';

export default {
  name: 'NavBar',
  components: {
    DropDown_Blok
  },
  props: {
    links: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
nav {
  /* Ajoutez votre style ici */
}
</style>