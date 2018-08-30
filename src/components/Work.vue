<template>
  <section>
    <a id="work"></a>
    <v-layout row class="text-xs-center mt-3">
      <v-flex xs10 offset-xs1>
        <h1 text-xs-center class="display-1">Work</h1>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3">
      <v-flex xs12>
        <hr>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3" v-for="(job, index) in jobs" :key="index">
      <v-flex xs12>
        <v-card>
          <v-layout row>
              <v-card-text class="title">{{job.company}}</v-card-text>
          </v-layout>
          <v-layout row>
            <v-card-text class="subheading">{{job.title}} | {{job.dates}}</v-card-text>
          </v-layout>
          <v-layout row>
            <v-card-text>{{job.desc}}</v-card-text>
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
  import WorkExperience from './WorkExperience.vue'

  export default {
    components: {WorkExperience},
    data () {
      return {
        jobs: [{company: 'Spill.ai', title: 'Junior Developer', dates: 'July 2018 - September 2018', desc: 'Created a mobile responsive User Interface using Vue.js, integrating many UI components on a best use-case basis. These include implementing Auto-completes, routing, date-pickers, search filters, and pagination. Also participated in design meetings about the App layout, and stand ups about the weeks progress. Worked on the API, using C# and .NET Core, creating methods to retrieve the appropriate information for all the endpoints, including meta-data. Additionally wrote unit tests to document that they were working as intended.'},
          {company: 'Intech Southwest Services', title: 'Warehouse Technician', dates: 'August 2016 - July 2017', desc: 'Performed QA and testing on hardware components prior to delivery and deployment for production. Developed a system that maintained hardware inventory in an effort to automate purchase order fulfillment requirements.'}]
      }
    }
  }
</script>
