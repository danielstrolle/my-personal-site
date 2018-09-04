<template>
  <section>
    <mq-layout mq="mobile">
      <v-flex xs12 v-for="(activity, index) in activities" :key="index">
        <v-layout row class="mt-3">
          <v-flex xs12 class="text-xs-center">
            <v-icon>{{activity.icon}}</v-icon>
            <h1 class="title mt-4">{{activity.title}}</h1>
          </v-flex>
        </v-layout>
        <v-layout row mt-4>
          <v-flex xs12>
            <p>{{activity.desc}}</p>
            <ul v-for="item in activity.list">
              <li>{{item}}</li>
            </ul>
          </v-flex>
        </v-layout>
      </v-flex>
    </mq-layout>
    <mq-layout mq="desktop">
      <v-flex xs8 offset-xs2>
        <v-layout row>
          <v-flex sm4 v-for="(activity, index) in activities" :key="index">
            <v-layout row class="mt-3">
              <v-flex sm10 offset-sm1 class="text-xs-center">
                <v-icon>{{activity.icon}}</v-icon>
                <h1 class="title mt-4">{{activity.title}}</h1>
              </v-flex>
            </v-layout>
            <v-layout row mt-4>
              <v-flex sm10 offset-sm1>
                <p>{{activity.desc}}</p>
                <ul v-for="item in activity.list">
                  <li>{{item}}</li>
                </ul>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
    </mq-layout>
  </section>
</template>

<script>
  export default {
    props: ['activities']
  }
</script>
