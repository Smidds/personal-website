<template>
  <div id="app">
    <Hello />
    <Work />
    <Projects />
    <Contact />
  </div>
</template>

<script>
  import Hello from './components/Hello.vue'
  import Work from './components/Work.vue'
  import Projects from './components/Projects.vue'
  import Contact from './components/Contact.vue'

  export default {
    name: 'app',
    components: {
      Hello,
      Work,
      Projects,
      Contact
    }
  }
</script>

<style lang="scss">
  @import 'assets/main.css';
</style>
