<template>
  <div id="home">
    <div class="desktop" style="display: flex; align-items: center; margin-top: 5rem;">
      <div style="width: 60%">
        <HomeTitle/>
      </div>
      <div style="width: 40%">
        <img src="../assets/logo.png" alt="logo" style="width: 250px; height: 250px">
      </div>
    </div>
    <div class="mobile">
      <div style="margin-top: 3rem">
        <HomeTitle/>
      </div>
      <img src="../assets/logo.png" alt="logo" style="width: 250px; height: 250px; margin-top: 2rem">
    </div>

  </div>
</template>

<script>
import HomeTitle from "@/parts/HomeTitle";
export default {
  name: "HomePage",
  components: {HomeTitle}
}
</script>

<style scoped>

</style>
