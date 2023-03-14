<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Your best adventure's partner!
    </p>
    <h4>More to come...</h4>
    <h3>See you here</h3>
    <ul>
      <li><a href="https://github.com/teschiopol" target="_blank" rel="noopener"><i class="fa-brands fa-github icon"/></a></li>
      <li><a href="https://www.linkedin.com/in/paolo-c-42bba9124/" target="_blank" rel="noopener"><i class="fa-brands fa-linkedin icon"/></a></li>
      <li><a href="https://twitter.com/teschiopol" target="_blank" rel="noopener"><i class="fa-brands fa-twitter icon"/></a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 20px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.icon{
  width: 25px;
  height: 25px;
}
</style>
