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

<style lang="scss" scoped>
  .contact-button {
    display: block;
    text-decoration: none;
    color: black;
    border: 2px solid black;
    padding: 22px 18px 22px 15px;
    margin-bottom: 15px;
    box-shadow: 0 4px 4px 0 rgba(0,0,0,0.45),0 4px 4px 0 rgba(0,0,0,0.12);
  }

  .contact-button:hover {
    background-color: #ffff4db3;
  }

  @media screen and (min-width: 801px) {
    .contact-button {
      flex: 0 calc(45% - 10px);
    }

    .contact-methods {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
  }
</style>