<template>
  <div class="navbar">
    <ul>
      <li v-for="(nav_elem, index) in nav_elements" :key="index" class="navbar-element">
        <a :href="nav_elem.link" class="navbar-link">
          <img :src="nav_elem.image" class="navbar-link__icon" />
          {{ nav_elem.name }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
  import icon_me from '../assets/icons/me.svg'; 
  import icon_work from '../assets/icons/work.svg';
  import icon_projects from '../assets/icons/projects.svg';
  import icon_mailbox from '../assets/icons/mailbox.svg';

  export default {
    name: 'Navigation-Bar',
    data() {
      return {
        nav_elements: [
          {
            'name': 'Home',
            'link': '#hello',
            'image': icon_me
          },
          {
            'name': 'Work',
            'link': '#work',
            'image': icon_work
          },
          {
            'name': 'Projects',
            'link': '#projects',
            'image': icon_projects
          },
          {
            'name': 'Contact',
            'link': '#contact',
            'image': icon_mailbox
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .navbar {
    display: flex;
    flex-direction: column;
  }

  .navbar-link {
    display: flex;
    flex-wrap: wrap;
    height: 55px;
    justify-content: center;
    padding: 5px 15px 25px 15px;
    width: 55px;
  }

  .navbar-link__icon {
    flex: 1 100%;
    height: 50px;
    width: 50px;
  }

  .navbar-element {
    display: inline-block;
    border: 2px solid black;
    box-shadow: 0 4px 4px 0 rgba(0,0,0,0.45),0 4px 4px 0 rgba(0,0,0,0.12);
    color: black;
    list-style: none;
    margin-bottom: 15px;
  }

  .navbar-element:hover {
    background-color: #ffff4db3;
  }
</style>