<template>
  <section>
    <a id="personal"></a>
    <v-layout row class="text-xs-center mt-3">
      <v-flex xs10 offset-xs1>
        <h1 class="display-1">Personal</h1>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3">
      <v-flex xs12>
        <hr>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-3">
      <v-flex xs12>
        Aside from Software Development, there are a few things in life that I enjoy, and here's a look into that.
      </v-flex>
    </v-layout>
    <PersonalActivity></PersonalActivity>
  </section>
</template>

<script>
  import PersonalActivity from './PersonalActivity.vue'

  export default {
    components: {PersonalActivity}
  }
</script>
