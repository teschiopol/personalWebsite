<template>
  <img alt="Vue logo" src="./assets/logo.png"  style="width:256px;height:256px;" @click="toggle(!isDarkMode)">
  <HelloWorld msg="Unicorne"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      isDarkMode: false
    }
  },
  methods: {
    toggle(payload){
      this.isDarkMode = payload;
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
