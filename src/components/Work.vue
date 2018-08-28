<template>
  <v-flex xs12 text-xs-center style="background-color: lightgray">
    <v-layout row>
      <v-flex xs12 mt-5>
        <v-flex xs4 offset-xs4>
          <h4 class="display-2">Work</h4>
        </v-flex>
      </v-flex>
    </v-layout>
    <v-layout row>
      <v-flex xs12 mt-3>
        <v-flex xs6 offset-xs3>
          <p style="font-size: 1.2em">
            My experiences thus far have allowed me to continue to pickup new pieces, understand overarching trends and themes, and put the puzzle together. The right opportunity is always right around the corner.
          </p>
        </v-flex>
      </v-flex>
    </v-layout>
    <v-layout row>
      <v-flex xs4 offset-xs4 mt-3>
        <h4 class="display-2">Experience</h4>
      </v-flex>
    </v-layout>
    <WorkExperience></WorkExperience>
  </v-flex>
</template>

<script>
  import WorkExperience from './WorkExperience.vue'

  export default {
    components: {WorkExperience}
  }
</script>
