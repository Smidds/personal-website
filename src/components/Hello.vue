<template>
  <div id="hello" class="hello-block">
    <h1>Hi. I'm <span class="full-name"><span class="text-highlight">Isaac Smith</span>.</span></h1>
    <div class="hello-block__blurb">
      I am a web developer, software engineer, data analysis enthusiast, politically active, outdoor-loving, 
      constantly curious individual who loves a good challenge and a stimulating project.
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Hello'
  }
</script>

<style scoped>
  .full-name {
    padding-left: 2px;
    display: inline-block;
    text-transform: uppercase;
  }
</style>
