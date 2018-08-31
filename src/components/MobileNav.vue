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
          <v-icon>menu</v-icon>
        </v-btn>
        <v-list>
          <v-list-tile
            v-for="(item, index) in items"
            :key="index"
            @click="">
            <v-list-tile-title v-scroll-to="item.link">{{item.title}}</v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-menu>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
  export default {
    data() {
      return {
        items: [
          {title: 'Projects', link: '#projects'},
          {title: 'Work', link: '#work'},
          {title: 'Personal', link: '#personal'}
        ]
      }
    }
  }
</script>
