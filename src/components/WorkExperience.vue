<template>
  <v-flex xs12 text-xs-left>
    <v-layout row mt-5>
      <v-flex xs8 offset-xs2>
        <v-card>
          <v-container fluid grid-list-lg>
            <v-layout row>
              <v-flex xs4>
                <h1>{{experience1.title}}</h1>
                <h2>{{experience1.dates}}</h2>
              </v-flex>
              <v-flex xs8>
                <ul v-for="desc in experience1.description">
                  <li>{{desc}}</li>
                </ul>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row mt-5>
      <v-flex xs8 offset-xs2>
        <v-card>
          <v-container fluid grid-list-lg>
            <v-layout row>
              <v-flex xs4>
                <h1>{{experience2.title}}</h1>
                <h2>{{experience2.dates}}</h2>
              </v-flex>
              <v-flex xs8>
                <ul v-for="desc in experience2.description">
                  <li>{{desc}}</li>
                </ul>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </v-flex>
</template>

<script>
  export default {
    data () {
      return {
        experience1: {
          title: 'Spill.ai',
          dates: 'July 2018 - September 2018',
          description: ['Created a mobile responsive User Interface using Vue.js, integrating many UI components on a best use-case basis. These include implementing Auto-completes, routing, date-pickers, search filters, and pagination. Also participated in design meetings about the App layout, and stand ups about the weeks progress.', ' Worked on the API, using C# and .NET Core, creating methods to retrieve the appropriate information for all the endpoints, including meta-data. Additionally wrote unit tests to document that they were working as intended.']
        },
        experience2: {
          title: 'Intech Southwest',
          dates: 'August 2016 - July 2017',
          description: ['Ensured hardware was functional and ready to use, then delivered and deployed to site.', 'Maintained customer relationships while servicing, replacing, or repairing their hardware.', 'Kept inventory of hardware received to fill purchase orders.']
        }
      }
    }
  }
</script>
