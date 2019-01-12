<template>
  <div id="projects">
    <Divider />
    <h2 class="section-header">
      Projects
    </h2>
    <div v-for="project in projects" :key="project.id">
      <h3 class="project-title">
        {{ project.title }}
      </h3>
      <div class="project-details">
        <p>
          {{ project.description }}
        </p>
        <div class="project-links">
          <ul class="project-links__large">
            <li v-for="link in project.relaventLinks" :key="link.id">
              {{ link.name }} <a :href="link.url">{{ link.url }}</a>
            </li>
          </ul>
          <ul class="project-links__small">
            <li v-for="link in project.relaventLinks" :key="link.id">
              <a :href="link.url">{{ link.name }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import projects_json from '../assets/projects.json';
  import Divider from './Divider';

  export default {
    name: 'Projects',
    components: {
      Divider
    },
    data() {
      return {
        projects: projects_json
      }
    }
  }
</script>

<style scoped>
  @media screen and (max-width: 450px) {
    .project-links__large {
      display: none;
    }
  }

  @media screen and (min-width: 451px) {
    .project-links__small {
      display: none;
    }
  }
</style>