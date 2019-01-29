<template>
  <div id="app">
    <Hello />
    <Work />
    <Projects />
    <Contact />
    <NavigationBar />
  </div>
</template>

<script>
  import Hello from './components/Hello.vue';
  import Work from './components/Work.vue';
  import Projects from './components/Projects.vue';
  import Contact from './components/Contact.vue';
  import NavigationBar from './components/Navbar.vue';

  export default {
    name: 'app',
    components: {
      Hello,
      Work,
      Projects,
      Contact,
      NavigationBar
    }
  }
</script>

<style lang="scss">
  @import 'assets/main.css';
</style>
