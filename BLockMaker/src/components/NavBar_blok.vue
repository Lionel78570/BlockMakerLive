<template>
    <nav>
      <ul>
        <NavItem v-for="link in links" :key="link.path" :link="link" />
      </ul>
    </nav>
  </template>
  
  <script>
  import NavItem from './NavItem.vue'
  
  export default {
    name: 'NavBar',
    components: {
      NavItem
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