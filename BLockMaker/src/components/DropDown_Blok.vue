<template>
    <div class="dropdown">
      <label class="dropdown-label" @click="toggleOptions">{{ label }}</label>
      <ul class="dropdown-options" :class="{ 'show': showOptions }">
        <li v-for="option in options" :key="option" @click="selectOption(option)">{{ option }}</li>
      </ul>
    </div>
</template>
  
<script>
  export default {
    props: {
      label: {
        type: String,
        required: true
      },
      options: {
        type: Array,
        required: true
      },
      selectedOption: {
        type: String,
        default: ''
      }
    },
    data() {
      return {
        showOptions: false
      };
    },
    methods: {
      toggleOptions() {
        this.showOptions = !this.showOptions;
      },
      selectOption(option) {
        this.showOptions = false;
        this.$emit('update:selectedOption', option);
      }
    }
  };
</script>
  
<style>
  .dropdown {
    position: relative;
    display: inline-block;
  }
  
  .dropdown-label {
    cursor: pointer;
  }
  
  .dropdown-options {
    position: absolute;
    top: 100%;
    left: 0;
    display: none;
    list-style: none;
    padding: 0;
    margin: 0;
    background-color: red;
    border: 1px solid white;
    border-top: none;
    z-index: 1;
  }
  
  .dropdown-options.show {
    display: block;
  }
  
  .dropdown-options li {
    padding: 8px;
    cursor: pointer;
  }
  
  .dropdown-options li:hover {
    background-color: green;
  }
</style>