<template>
  <section class="mt-3">
    <a id="projects"></a>
    <v-layout row class="text-xs-center mt-3">
      <v-flex xs10 offset-xs1>
        <h1 text-xs-center class="display-1">Projects</h1>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3">
      <v-flex xs12>
        <hr>
      </v-flex>
    </v-layout>
    <v-layout row v-for="(proj, index) in projects" :key="index">
      <v-flex xs12>
        <v-card class="mt-3">
          <v-card-text class="title text-xs-center">{{proj.title}}</v-card-text>
          <v-flex xs10 offset-xs1>
            <hr>
          </v-flex>
          <v-flex xs12 v-if="proj.img">
            <v-card-text class="text=xs-center subheading">Desktop View</v-card-text>
            <v-card-media :src=proj.img height="300"></v-card-media>
          </v-flex>
          <v-card-text>{{proj.desc}}</v-card-text>
          <v-flex xs10 offset-xs1>
            <hr>
          </v-flex>
          <v-card-text v-html="'<strong>Languages/Frameworks used: </strong>' + techArrayToString(proj.tech)">
          </v-card-text>
          <v-flex text-xs-center v-if="proj.sourceCode">
            <a :href=proj.sourceCode style="text-decoration: none;">View Source Code</a>
          </v-flex>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row class="text-xs-center mt-3">
      <v-flex xs10 offset-xs1>
        <h1 text-xs-center class="display-1">More Projects</h1>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3">
      <v-flex xs12>
        <hr>
      </v-flex>
    </v-layout>
    <v-carousel class="mt-3"
      hide-delimiters
      style="height: 100%;"
    >
      <v-carousel-item  v-for="(proj, index) in moreProjects" :key="index">
        <v-card class="mt-3">
          <v-card-text class="title text-xs-center">{{proj.title}}</v-card-text>
          <v-flex xs10 offset-xs1>
            <hr>
          </v-flex>
          <v-flex xs12 v-if="proj.img">
            <v-card-text class="text=xs-center subheading">Desktop View</v-card-text>
            <v-card-media :src=proj.img height="300"></v-card-media>
          </v-flex>
          <v-card-text>{{proj.desc}}</v-card-text>
          <v-flex xs10 offset-xs1>
            <hr>
          </v-flex>
          <v-card-text v-html="'<strong>Languages/Frameworks used: </strong>' + techArrayToString(proj.tech)">
          </v-card-text>
          <v-flex text-xs-center v-if="proj.sourceCode">
            <a :href=proj.sourceCode style="text-decoration: none;">View Source Code</a>
          </v-flex>
        </v-card>
      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        projects: [{
          title: 'danielstrolle@github.io',
          desc: 'The site you are on right now! Built using Vue.js and Vuetify, this mobile responsive site has a user-friendly and intuitive UI to highlight my work thus far in my career.',
          tech: ['Vue.js', 'Vuetify', 'Vue MQ', 'Javascript', 'CSS'],
          sourceCode: 'https://github.com/danielstrolle/my-project'
        },
          {
            title: 'Spill.ai',
            desc: 'Responsible for developing a responsive, mobile-first UI using Vue.JS. Designed, implemented, and tested components based on use-case and cost analysis. The solution contained auto-complete functionality, request routing, date and search filtration, and paginating lazy-loaded results. Participated in design meetings to assist app business and technical requirements and weekly stand-ups for team progress.',
            img: '/static/img/projects/spill.ai-ss-desktop.png',
            tech: ['C#', '.NET Core', 'Elasticsearch', 'MSTest', 'npm', 'Vue.js', 'Vuetify', 'Vue MQ', 'Javascript', 'jQuery', 'CSS']
          },
          {
            title: 'livemusicismy.life',
            desc: 'In two weeks time, created and launched an application that uses geolocated data sources to suggest live music near users. Users can add and track shows with their own accounts and review shows they’ve been to.',
            img: '/static/img/projects/lmiml-ss.png',
            tech: ['Spring', 'Tomcat', 'Java', 'JavaScript', 'jQuery', 'Materialize', 'CSS'],
            sourceCode: 'https://github.com/daniel-carlo-tomas/songkick_mockup'
          }
        ],
        moreProjects: [{
          title: 'AWS Serverless Portfolio',
          desc: 'Hosted and Deployed a serverless personal portfolio, that automatically kicks off a build and deployment if code is changed and pushed to GitHub, where I keep the source code. Had fun working with AWS, and going through this process and playing with the different services and seeing how they work together.',
          img: '/static/img/projects/aws-serverless.png',
          tech: ['Amazon Web Services', 'React', 'Babel', 'Webpack', 'npm', 'Jest', 'Chai & Mocha', 'HTML', 'CSS', 'GitHub'],
          sourceCode: 'https://github.com/danielstrolle/my-portfolio'
        },
          {
            title: 'blog.danielstrolle.me',
            desc: 'A personal blog built as an exercise to explore controllers, models, and views as a web architecture framework. Featured implementation of the repository design paradigm, and OAuth security protocol. Expanded to allow users to create their own blog posts.',
            img: '/static/img/projects/blog-ss.png',
            tech: ['Spring', 'Java', 'Javascript', 'Bootstrap', 'CSS'],
            sourceCode: 'https://github.com/danielstrolle/springboot-blog'
          },
          {
            title: 'Dab-lister (ad-lister)',
            desc: 'Using Java, create an application that uses controllers, models, and DAOs to present different JSPs based on user actions. A mock-up with a twist based on ebay, allows users to register an account, then create ads for dabs. User can search through other posted dabs based off name or category',
            img: '/static/img/projects/adlister-ss.png',
            tech: ['Java', 'Javascript', 'Bootstrap', 'CSS'],
            sourceCode: 'https://github.com/B-A-D/Mr-Adlister'
          },
          {
            title: 'Ajax Weather Map',
            desc: 'Using AJAX requests, query the google maps API for a 3 day forecast on any given location. User may drag and drop pin to get the live 3-day forecast on that location using jQuery and event listeners. Use Javascript to live-update the html and Map.',
            img: '/static/img/projects/ajax-api-ss.png',
            tech: ['Javascript', 'jQuery', 'CSS', 'HTML'],
            sourceCode: 'https://github.com/Brandon-Daniel-Ajax/Ajax-API-Request'
          },
          {
            title: 'Monkey Business LLC',
            desc: 'Utilizing paired programming, built a web application that allows users to add, edit, rate, and delete movies. Used a JSON-server to mock our backend, implemented AJAX requests and fetches to update our HTML, through JavaScript, without needing to refresh.',
            img: '/static/img/projects/movie_db-ss.png',
            tech: ['Javascript', 'jQuery', 'CSS', 'HTML'],
            sourceCode: 'https://github.com/TravisAndDanielMovieApp/movies-application'
          }]
      }
    },
    methods: {
      techArrayToString: function (array) {
        let techString = ''
        array.forEach(function (tech) {
          techString += tech + ', '
        })
        let length = techString.length
        techString = techString.substring(0, length - 2)
        return techString
      }
    }
  }
</script>
