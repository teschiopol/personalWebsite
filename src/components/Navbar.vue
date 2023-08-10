<template>
  <div id="navbar">
    <nav>
      <div style="display: flex">
        <div id="logo" style="width: 25%" @click="toggle(!isDarkMode)">
          <img src="../assets/favicon.ico.png" alt="icon" style="width: 40px; height: 40px">
        </div>
        <div id="pages" class="navbar desktop">
          <div style="width: 10%;"></div>
          <div style="width: 20%">
            <a href="#">Home</a>
          </div>
          <div style="width: 20%">
            <a href="#project">Projects</a>
          </div>
          <div style="width: 20%">
            <a href="#stack">Stack</a>
          </div>
          <div style="width: 20%">
            <a href="#contact">Contact</a>
          </div>
        </div>
        <div id="menu" class="navbar mobile">
          <div style="width: 10%;"></div>
          <a v-show="!menu" @click="toggleMenu" class="open"><i class="fa-solid fa-bars" style="height: 20px; width: 20px;" /></a>
          <a v-show="menu" @click="toggleMenu" class="close"><i class="fa-solid fa-pause" style="height: 20px; width: 20px;" /></a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
import {onMounted, ref} from "vue";

export default {
    name: "NavbarPage",
    setup(){
      const isDarkMode = ref(false);
      const menu = ref(false);

      const toggle = (payload) => {
        isDarkMode.value = payload;
        document.documentElement.className = payload;
        localStorage.setItem('theme', payload);
      }

      const toggleMenu = () => {
        menu.value = !menu.value;
      }

      onMounted(function(){
        toggle(JSON.parse(localStorage.getItem('theme')));
      });

      // TODO: menu

      return{isDarkMode, menu, toggleMenu, toggle}
    }
  }
</script>

<style scoped>
  .navbar{
    width:75%;
    text-align: right;
    display: flex;
    align-items: center;
  }

  .mobile{
    flex-direction: row-reverse;
  }
</style>
