<template>
  <Navbar />
  <Home />
  <Project />
  <Stack />
  <Contact />
  <Footer />
</template>

<script>
  import Navbar from "@/components/Navbar";
  import Home from "@/components/Home";
  import Project from "@/components/Project";
  import Stack from "@/components/Stack";
  import Contact from "@/components/Contact";
  import Footer from "@/components/Footer";
  export default {
    name: 'App',
    components: {
      Navbar,
      Home,
      Project,
      Stack,
      Contact,
      Footer
    }
  }
</script>

<style>
  #app {
    font-family: Montserrat, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
  }

  * {
    background-color: var(--bg);
    color: var(--text);
  }

  a {
    color: var(--link);
  }
</style>
