<template>
  <img alt="Unicorne logo" src="./assets/logo.png"  style="width:256px;height:256px;" @click="toggle(!isDarkMode)">
  <HelloWorld msg="Unicorne"/>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import {onMounted, ref} from "vue";

  export default {
    name: 'App',
    components: {
      HelloWorld
    },
    setup(){
      const isDarkMode = ref(false);

      const toggle = (payload) => {
        isDarkMode.value = payload;
        document.documentElement.className = payload;
        localStorage.setItem('theme', payload);
      }

      onMounted(function(){
        toggle(JSON.parse(localStorage.getItem('theme')));
      });

      return{isDarkMode, toggle}
    }
  }
</script>

<style>
  #app {
    font-family: Montserrat, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin-top: 60px;
  }

  * {
    background-color: var(--bg);
    color: var(--text);
  }

  a {
    color: var(--link);
  }
</style>
