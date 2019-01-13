<template>
  <div id="projects">
    <Divider />
    <h2 class="section-header">
      Projects
    </h2>
    <div v-for="project in projects" :key="project.id" class="project">
      <h3 class="card-title">
        {{ project.title }}
      </h3>
      <div class="project-details">
        <p>
          {{ project.description }}
        </p>
        <div class="project-tags">
          <span v-for="(tag, index) in project.tags" :key="index" class="project-tag">
            {{ tag }}
          </span>
        </div>
        <div class="project-links" v-if="project.relaventLinks.length > 0">
          <p><i>Links:</i></p>
          <ul class="project-links__large">
            <li v-for="link in project.relaventLinks" :key="link.id" class="projects-link">
              {{ link.name }} <a :href="link.url">{{ link.url }}</a>
            </li>
          </ul>
          <ul class="project-links__small">
            <li v-for="link in project.relaventLinks" :key="link.id" class="projects-link">
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

<style lang="scss" scoped>
  .card-title {
    margin-top: 5px;
  }

  .project {
    border: 3px solid black;
    padding: 15px;
    margin-bottom: 32px;
  }

  .projects-link {
    margin: 0 0 18px 18px;
  }

  .projects-link a {
    color: black;
    text-decoration: underline;
  }

  .projects-link a:hover {
    background-color: #ffff4db3;
    text-decoration: none;
  }

  .project-links {
    border-top: 2px dashed #969696;
  }

  .project-links__small, .project-links__large {
    list-style: decimal-leading-zero;
  }

  .project-tag {
    border: 2px solid black;
    padding: 5px;
    display: inline-block;
    margin-right: 5px;
    margin-bottom: 5px;
  }

  .project-tags {
    margin-bottom: 15px;
  }

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