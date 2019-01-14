<template>
  <div id="app">
    <Hello />
    <Work />
    <Projects />
    <Contact />
    <NavigationBar :nav_elems="nav_elements"/>
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
    },
    data() {
      return {
        nav_elements: [
          {
            'name': 'Home',
            'link': '#hello',
            'image': ''
          },
          {
            'name': 'Work',
            'link': '#work',
            'image': ''
          },
          {
            'name': 'Projects',
            'link': '#projects',
            'image': ''
          },
          {
            'name': 'Contact',
            'link': '#contact',
            'image': ''
          }
        ]
      }
    }
  }
</script>

<style lang="scss">
  @import 'assets/main.css';
</style>
