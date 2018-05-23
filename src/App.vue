<template>
<div id="app">
  <v-app>
    <v-toolbar app dense>
      <v-toolbar-title>
        <router-link :to="{ name: 'home' }">CVBuilder</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-menu offset-y>
          <v-btn slot="activator" flat>Themes
            <v-icon dark>arrow_drop_down</v-icon>
          </v-btn>
          <v-list>
            <v-list-tile v-for="theme in allThemes" :key="theme"
                :to="{ name: 'resume', params: { resumeid: theme } }">
              <v-list-tile-title>{{ theme }}</v-list-tile-title>
            </v-list-tile>
          </v-list>
        </v-menu>
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
  name: 'app',
  data () {
    return {
      allThemes: [
        'left-right-rtl',
        'material-dark',
        'side-bar',
        'left-right',
        'oblique',
        'purple',
        'side-bar-rtl'
      ]
    };
  }
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
