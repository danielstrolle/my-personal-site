<template>
  <section class="mt-3">
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
    <PersonalActivity :activities="activities"></PersonalActivity>
  </section>
</template>

<script>
  import PersonalActivity from './PersonalActivity.vue'

  export default {
    components: {PersonalActivity},
    data () {
      return {
        activities: [
          {
            title: 'Fitness',
            icon: 'fitness_center',
            list: ['Basketball', 'Weightlifting', 'Sand-Volleyball', 'Football', 'Walking'],
            desc: 'Whether it be through competition, or just self-betterment, fitness gives me a way to push my body and test myself, constantly setting and meeting new goals. The temporary release from the stresses of life, also works to keep my mind fresh and productive. These are what I enjoy: '
          },
          {
            title: 'Cooking',
            icon: 'restaurant_menu',
            list: ['Baking', 'Stove-Top', 'Slow Cooker', 'Grilling'],
            desc: 'Although cleaning isn\'t the most fun, I love to cook! Cooking with others and trying new recipes is a fun social activity that makes me a more patient person. Getting to eat my own food is of course the best part! Here are my most common methods: '
          },
          {
            title: 'Gaming',
            icon: 'headset_mic',
            list: ['Counter-Strike: Global Offensive', 'League of Legends'],
            desc: 'PC Master Race of course, the competitive environment these games present allow me to have fun competing and testing my skill against others online. Sometimes I get a little too loud, what can I say, im passionate, but its always a good time. Here are the games I play: '
          }]
      }
    }
  }
</script>
