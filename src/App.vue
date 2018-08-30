<template>
  <v-app>
    <mq-layout mq="desktop">
      <DesktopNav></DesktopNav>
    </mq-layout>
    <mq-layout mq="mobile">
      <MobileNav></MobileNav>
    </mq-layout>
    <v-content>
      <Home/>
    </v-content>
    <v-footer
      height="auto"
      app
      absolute
    >
      <v-layout
        justify-center
        row
        wrap
      >
        <v-btn
          v-for="(l, index) in links"
          :key="index"
          flat
          round
        >
          <a :href="l.link" style="text-decoration: none; color: black;">
            {{ l.name }}
          </a>
        </v-btn>
        <v-flex
          lighten-2
          py-3
          text-xs-center
          xs12
        >
          &copy;2018 — <strong>Daniel Strolle</strong>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
  import Home from './components/Home'
  import DesktopNav from './components/DesktopNav.vue'
  import MobileNav from './components/MobileNav.vue'
  import Vue from 'vue'
  import VueMq from 'vue-mq'

  Vue.use(VueMq, {
    breakpoints: {
      mobile: 450,
      desktop: Infinity
    }
  })

  export default {
    data() {
      return {
        fixed: false,
        title: 'Daniel Strolle',
        links: [
          {name: 'Github', link: 'https://github.com/danielstrolle'},
          {name: 'LinkedIn', link: 'https://www.linkedin.com/in/danielstrolle/'},
          {name: 'Email Me', link: 'mailto:danielstrolle@gmail.com'}
        ]
      }
    },
    name: 'App',
    components: {
      Home,
      DesktopNav,
      MobileNav
    }
  }
</script>
