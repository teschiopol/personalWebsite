<template>
  <div class="desktop">
    <a class="text" href="https://open.spotify.com/playlist/4lh2i4fLX8V9XvgAE7pJwp?si=55ff3d656e634cdc" target="_blank"><i class="fa-brands fa-spotify"/> Listening on Spotify</a>
  </div>
  <h1 id="title" class="rainbow">
    Unicorne
  </h1>
  <h4 id="payoff">
    Great Things, Need Life
  </h4>
</template>

<script>
  export default {
    name: "HomeTitle"
  }
</script>

<style scoped>
  #title{
    font-size: 4rem;
    margin: 1rem auto;
  }

  .rainbow{
    background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(253,29,29,1) 50%, rgba(252,176,69,1) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
</style>
