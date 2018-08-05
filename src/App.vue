<template>
  <v-app>
    <v-toolbar dark app>
      <v-flex xs2>
        <v-toolbar-side-icon></v-toolbar-side-icon>
      </v-flex>
      <v-flex xs8>
        <v-toolbar-title>Vue.js Demo App</v-toolbar-title>
      </v-flex>
      <v-flex xs2>
        <v-btn icon>
          <v-icon>more_vert</v-icon>
        </v-btn>
      </v-flex>
    </v-toolbar>
    
    <v-content app>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
    
    <v-footer app dark height="auto">
      <v-card class="flex" flat tile>
        <v-card-actions class="grey darken-3 justify-center">
          &copy;2018 — &nbsp;<strong>Cooray</strong>
        </v-card-actions>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    name: 'app',
  };
</script>

<style>
  body {
    margin: 0;
  }
  
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  
  main {
    text-align: center;
    margin-top: 40px;
  }
  
  header {
    margin: 0;
    height: 56px;
    padding: 0 16px 0 24px;
    background-color: #35495E;
    color: #ffffff;
  }
  
  header span {
    display: block;
    position: relative;
    font-size: 20px;
    line-height: 1;
    letter-spacing: .02em;
    font-weight: 400;
    box-sizing: border-box;
    padding-top: 16px;
  }
</style>
