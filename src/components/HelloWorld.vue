<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Full Stack Developer w// 4 years of exp,<br>
      a lot of side projects!
    </p>
    <h4>More to come...</h4>
    <h3>Social Profiles</h3>
    <ul>
      <li><a href="https://github.com/teschiopol" target="_blank" rel="noopener">GitHub</a></li>
      <li><a href="https://www.linkedin.com/in/paolo-c-42bba9124/" target="_blank" rel="noopener">LinkedIn</a></li>
      <li><a href="https://twitter.com/teschiopol" target="_blank" rel="noopener">Twitter</a></li>
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>
