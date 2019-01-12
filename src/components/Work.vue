<template>
  <div id="work">
    <Divider />
    <h2 class="section-header">Work History</h2>
    <div v-for="job in $options.work_history" :key="job.id">
      <h3 class="job-title">
        {{ job.title }}
      </h3>
      <div class="job-details">
        <span class="job-details__start-date"> {{ job.startDate }} </span>
        <span class="job-details__end-date"> {{ job.endDate }} </span>
        <span class="job-details__company-name"> {{ job.company }} </span>
        <span class="job-details__company-location"> {{ job.location }} </span>
      </div>
      <p class="job-description">
        {{ job.description }}
      </p>
    </div>
  </div>
</template>

<script>
  import work_history_json from '../assets/work_history.json';
  import Divider from './Divider'

  export default {
    name: 'Work',
    components: {
      Divider
    },
    work_history: work_history_json
  }
</script>

<style scoped>
</style>