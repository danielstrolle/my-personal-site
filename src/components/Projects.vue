<template>
  <section>
    <v-layout row class="text-xs-center mt-3">
      <v-flex xs10 offset-xs1>
        <h1 text-xs-center class="display-1">Projects</h1>
      </v-flex>
    </v-layout>
    <v-layout row v-for="(proj, index) in projects" :key="index">
      <v-flex xs12>
        <v-card class="mt-3">
          <v-card-title class="text-xs-center">{{proj.title}}</v-card-title>
          <v-card-media :src=proj.img height="400"></v-card-media>
          <v-flex xs12 v-if="proj.img2">
            <v-card-text class="text=xs-center">Mobile View</v-card-text>
            <v-card-media :src=proj.img2 height="400"></v-card-media>
          </v-flex>
          <v-card-text>{{proj.desc}}</v-card-text>
          <!--ADD TECH USED AND LINKS TO SITE/GITHUB-->
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        projects: [
          {title: 'Spill.ai', desc: 'Responsible for developing a responsive, mobile-first UI using Vue.JS.\n' +
          'Designed, implemented, and tested components based on use-case and cost analysis.\n' +
          'The solution contained auto-complete functionality, request routing, date and search filtration, and paginating lazy-loaded results.\n' +
          'Participated in design meetings to assist app business and technical requirements and weekly stand-ups for team progress.', img: '/static/img/projects/spill.ai-ss-desktop.png', img2: '/static/img/projects/spill.ai-ss-mobile.png'},
          {title: 'AWS Serverless Portfolio', desc: 'Hosted and Deployed a serverless personal portfolio, that automatically kicks off a build and deployment if code is changed and pushed to GitHub, where I keep the source code. Had fun working with AWS, and going through this process and playing with the different services and seeing how they work together.', img: '/static/img/projects/aws-servless.png'}
          ]
      }
    }
  }
</script>
