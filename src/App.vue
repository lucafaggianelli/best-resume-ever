<template>
<div id="app">
  <v-app>
    <v-toolbar app dense>
      <v-toolbar-title>
        <router-link :to="{ name: 'home' }">CVBuilder</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat>Link One</v-btn>
        <v-btn flat>Link Two</v-btn>
        <v-btn flat>Link Three</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
  </v-app>
</div>
</template>

<script>
export default {
  name: 'app'
};
</script>

<style>
/* Add new fonts here */
@import '../node_modules/roboto-fontface/css/roboto/roboto-fontface.css';
@import '../node_modules/font-awesome/css/font-awesome.css';
@import '../node_modules/material-design-icons/iconfont/material-icons.css';
@import '../node_modules/source-sans-pro/source-sans-pro.css';
@import '../node_modules/npm-font-open-sans/open-sans.css';
@import '../node_modules/npm-font-open-sans-condensed/open-sans-condensed.css';
@import '../node_modules/raleway-webfont/raleway.css';
body {
  padding: 0;
  margin: 0;
  overflow-x: hidden;
}
</style>
