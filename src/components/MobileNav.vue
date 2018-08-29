<template>
  <v-toolbar
    app
  >
    <v-toolbar-items>
      <v-menu offset-y>
        <v-btn
          flat
          slot="activator"
        >
          <v-icon>child_care</v-icon>
        </v-btn>
        <v-list>
          <v-list-tile
            v-for="(item, index) in items"
            :key="index"
            @click="">
            <v-list-tile-title>{{item.title}}</v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-menu>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {title: 'Work'},
          {title: 'Projects'},
          {title: 'Personal'}
        ]
      }
    }
  }
</script>
