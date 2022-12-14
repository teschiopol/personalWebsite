<template>
  <img alt="Vue logo" src="./assets/logo.png" width="256" height="256">
  <HelloWorld msg="Unicorne by Paolo Concolato"/>
  <DarkModeToggle/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DarkModeToggle from "@/components/DarkModeToggle";

export default {
  name: 'App',
  components: {
    HelloWorld,
    DarkModeToggle
  }
}
</script>

<style>

@import '@/styles/dark.css';
@import '@/styles/light.css';

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
