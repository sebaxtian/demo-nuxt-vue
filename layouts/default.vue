<template>
  <v-app>
    <v-navigation-drawer clipped fixed v-model="drawer" app class="light-green accent-1">
      <v-list dense class="light-green accent-1">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>dashboard</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Dashboard</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Settings</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left color="light-green" dark>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title> {{ title }} </v-toolbar-title>
    </v-toolbar>
    <v-content>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer app fixed color="light-green" dark>
      <v-layout row wrap justify-center>
        <span class="caption">
          <strong>
            &copy; 2018 ~ <a href="http://about.me/sebaxtian" target="_blank" style="color: inherit; text-decoration: none">about.me/sebaxtian</a>
          </strong>
        </span>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: function () {
      return {
        title: 'Aplicación',
        drawer: false
      }
    }
  }
</script>
