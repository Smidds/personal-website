<template>
  <div id="work">
    <Divider />
    <h2 class="section-header">Work History</h2>
    <div class="card-list">
      <div v-for="job in $options.work_history" :key="job.id" class="job card">
        <h3 class="card-title">
          {{ job.title }}
        </h3>
        <div class="job-details">
          <div class="job-details__dates">
            <span class="job-details__start-date"> {{ get_date(job.startDate) }} - </span>
            <span class="job-details__end-date"> {{ get_date(job.endDate) }} </span>
          </div>
          <span class="job-details__company-name"> <i>{{ job.company }}</i> </span>
          <span class="job-details__company-location"> {{ job.location }} </span>
        </div>
        <p class="job-description">
          {{ job.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  import work_history_json from '../assets/work_history.json';
  import Divider from './Divider'

  var date_conversion = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']

  export default {
    name: 'Work',
    components: {
      Divider
    },
    methods: {
      get_date: (date_str) => {
        if (date_str === '') {
          return 'Present'
        }
        
        var new_date = new Date(date_str);
        var month_str = date_conversion[new_date.getMonth()];
        month_str += ` ${new_date.getFullYear()}`
        return month_str;
      }
    },
    work_history: work_history_json
  }
</script>

<style lang="scss" scoped>
  .job {
    border: 3px solid black;
    padding: 15px;
    margin-bottom: 32px;
  }
  
  .job-details__company-name {
    padding-left: 15px;
    display: block;
    text-indent: -15px;
  }

  .job-details {
    margin-bottom: 35px;
    border-bottom: 2px dashed #969696;
    padding-bottom: 15px;
  }

  .job-details > * {
    font-size: 16px;
    margin-bottom: 5px;
    color: #5c5c5c;
  }
</style>