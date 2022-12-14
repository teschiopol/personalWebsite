<template>
  <button class="button" @click="toggle(!isDarkMode)">{{isDarkModeLabel}}</button>
</template>

<script>
  export default {
    name: 'DarkModeToggle',

    data() {
      return {
        isDarkMode: false,
        isDarkModeLabel: "Light"
      }
    },

    methods: {
      toggle(payload){
        this.isDarkMode = payload;
        this.isDarkModeLabel = payload ? 'Dark' : 'Light';
        document.documentElement.className = payload;
        localStorage.setItem('theme', payload);
      }
    },

    mounted() {
      this.toggle(JSON.parse(localStorage.getItem('theme')));
    }
  }
</script>

<style>
  .button{
    margin: 30px 0 30px;
    font-size: 15px;
  }
</style>
