<template>
 <v-app>
  <v-toolbar dark color="primary">
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title class="white--text">Title</v-toolbar-title>
    <v-spacer></v-spacer>
        <v-flex xs8>
            <v-text-field
              v-on:keyup.enter="search"
              v-model="searchField"
              name="search"
            ></v-text-field>
          </v-flex>
    <v-btn icon @click="search">
      <v-icon>search</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>apps</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>refresh</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>more_vert</v-icon>
    </v-btn>
  </v-toolbar>
  <main>
    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
  </main>
  <v-footer app></v-footer>
</v-app>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      searchField: ''
    }
  },
  methods: {
    search () {
      console.log(this.searchField)
    }
  }
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
