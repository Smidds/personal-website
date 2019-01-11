<template>
  <div id="app">
    <Hello />
    <Work />
    <Contact />
  </div>
</template>

<script>
  import Hello from './components/Hello.vue'
  import Work from './components/Work.vue'
  import Contact from './components/Contact.vue'

  export default {
    name: 'app',
    components: {
      Hello,
      Work,
      Contact
    }
  }
</script>

<style>
  #app {
    font-family: 'Inconsolata', monospace;
  }

  p {
    font-family: 'Montserrat', sans-serif;
  }
</style>
