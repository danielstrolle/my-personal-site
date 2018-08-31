<template>
  <section>
    <mq-layout mq="mobile">
      <v-layout row>
        <v-flex xs10 offset-xs1>
          <h1 class="display-2 text-xs-center">Daniel Strolle</h1>
          <h2 class="Title text-xs-center">Junior Developer @ Spill.ai</h2>
        </v-flex>
      </v-layout>
      <v-layout row mt-3>
        <v-flex xs12>
          <h4 class="title text-xs-center">Certifications</h4>
          <br>
          <hr>
          <ul class="mt-3">
            <li>OCA Java SE 8 Programmer</li>
            <li>Codeup - Certificate of Completion</li>
          </ul>
        </v-flex>
      </v-layout>
      <v-layout row mt-3>
        <v-flex xs12>
          <v-card>
            <v-container fluid grid-list-lg>
              <v-card-text>
                My experiences thus far have allowed me to continue to pickup new pieces, understand overarching trends and themes, and put the puzzle together. The right opportunity is always right around the corner!
              </v-card-text>
            </v-container>
          </v-card>
        </v-flex>
      </v-layout>
    </mq-layout>
    <mq-layout mq="desktop">
      <v-layout row>
        <v-flex sm4 offset-sm2>
          <h1 class="display-2">Daniel Strolle</h1>
          <h2 class="Title">Junior Developer @ Spill.ai</h2>
        </v-flex>
        <v-flex sm2 offset-sm2>
          <h2 class="Title text-xs-center">Certifications</h2>
          <hr>
          <ul class="mt-3">
            <li>OCA Java SE 8 Programmer</li>
            <li>Codeup - Certificate of Completion</li>
          </ul>
        </v-flex>
      </v-layout>
    </mq-layout>
  </section>
</template>

<script>
  export default {}
</script>
