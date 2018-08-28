<template>
  <v-flex xs12>
    <Parallax></Parallax>
    <v-container fluid>
      <Bio></Bio>
      <Work></Work>
    </v-container>
  </v-flex>
</template>

<script>
  import Parallax from './Parallax.vue'
  import Bio from './Bio.vue'
  import Work from './Work.vue'

  export default {
    components: {Parallax, Bio, Work}
  }
</script>
