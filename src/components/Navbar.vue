<template>
  <div class="navbar">
    <a v-for="(nav_elem, index) in nav_elems" :key="index" :href="nav_elem.link">
      {{ nav_elem.name }}
    </a>
  </div>
</template>

<script>
  export default {
    name: 'Navigation Bar',
    props: ['nav_elems']
  }
</script>

<style scoped>

</style>