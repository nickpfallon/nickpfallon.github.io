<template>
  <div id="app">
    <v-app>
      <v-navigation-drawer persistent dark v-model="drawer" overflow class="nav-drawer">
        <v-toolbar flat>
          <v-list class="pa-0">
            <v-list-tile avatar>
              <v-list-tile-avatar>
                <img src="/static/avatar.png" />
              </v-list-tile-avatar>
              <v-list-tile-content>
                <v-list-tile-title>Nick Fallon</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-toolbar>
        <v-list class="pt-0" dense>
          <v-divider></v-divider>
          <v-list-tile v-for="item in items" :key="item.title" @click="" :href="item.route">
            <v-list-tile-action>
              <v-icon class="white--text">{{ item.icon }}</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
      <v-toolbar fixed class="cyan darken-4">
        <v-toolbar-side-icon @click.stop="drawer = !drawer" class="white--text"></v-toolbar-side-icon>
        <v-toolbar-title class="toolbar-title">nick fallon</v-toolbar-title>
        <v-spacer></v-spacer>
        <a href="https://github.com/nickpfallon" target="_blank"><v-btn icon>
          <v-icon class="white--text">fa-github</v-icon>
        </v-btn></a>
        <a href="https://www.linkedin.com/in/nickpfallon/" target="_blank"><v-btn icon>
          <v-icon class="white--text">fa-linkedin</v-icon>
        </v-btn></a>
        <a href="mailto:nickfallonwastaken@gmail.com"><v-btn icon>
          <v-icon class="white--text">fa-envelope-o</v-icon>
        </v-btn></a>
      </v-toolbar>
      <main>
        <v-container fluid>
          <router-view></router-view>
        </v-container>
      </main>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
      return {
        drawer: true,
        items: [
          { title: 'Home', icon: 'fa-home', route: '/#/' },
          { title: 'About', icon: 'fa-question', route: '/#/about' },
          { title: 'Projects', icon: 'fa-flask' , route: '/#/projects'},
          { title: 'Contact Me', icon: 'fa-comment-o', route: '/#/contact' },
          { title: 'Resume', icon: 'fa-file-text-o', route: '../static/NicholasFallon-Resume.pdf'}
        ],
        right: null
      }
    }
}
</script>
<style>
body {
  margin: 0;
  font-family: 'Josefin Sans', Helvetica, sans-serif;
}
.container {
  padding: 0;
}
.toolbar-title {
  color: #fafafa;
}
a {
  text-decoration: none;
}
/*.nav-drawer {
  opacity: .5;
}*/

</style>
