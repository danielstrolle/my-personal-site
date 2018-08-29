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
    <v-footer app absolute>
      <span>&copy; 2017</span>
      <span>Contact Me</span>
      <span>email</span>
      <span>linkedin</span>
      <span>github</span>
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
    data () {
      return {
        fixed: false,
        title: 'Daniel Strolle'
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
