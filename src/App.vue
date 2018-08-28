<template>
  <v-app>
    <v-toolbar
      app
      row
    >
      <v-toolbar-items>
        <v-btn flat>Work</v-btn>
        <v-btn flat>Projects</v-btn>
        <v-btn flat>Personal</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <HelloWorld/>
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
import HelloWorld from './components/HelloWorld'

export default {
  data () {
    return {
      fixed: false,
      title: 'Daniel Strolle'
    }
  },
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
