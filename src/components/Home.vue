<template>
  <v-flex xs12>
    <Parallax></Parallax>
    <v-container fluid>
      <Bio></Bio>
      <Projects></Projects>
      <Work></Work>
      <Personal></Personal>
    </v-container>
  </v-flex>
</template>

<script>
  import Parallax from './Parallax.vue'
  import Bio from './Bio.vue'
  import Work from './Work.vue'
  import Projects from './Projects.vue'
  import Personal from './Personal.vue'

  export default {
    components: {Parallax, Bio, Work, Projects, Personal}
  }
</script>
