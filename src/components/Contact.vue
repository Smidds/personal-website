<template>
  <div>
    <Divider />
    <h2 class="section-header">
      Contact Me
    </h2>
    <div class="contact-methods">
      <a class="contact-button" href="mailto:isaachsmith.important.29@gmail.com" target="_top" rel="external">
        Email Me
      </a>
      <a class="contact-button" href="https://www.linkedin.com/in/isaac-harold-smith/" target="_blank" rel="external">
        Message on LinkedIn
      </a>
    </div>
  </div>
</template>

<script>
  import Divider from './Divider';

  export default {
    name: 'Contact',
    components: {
      Divider
    }
  }
</script>

<style scoped>
  .contact-button {
    display: block;
    text-decoration: none;
    color: black;
    border: 2px solid black;
    padding: 22px 0 22px 15px;
    margin-bottom: 15px;
  }

  .contact-button:last-child {
    margin-bottom: 0;
  }
</style>