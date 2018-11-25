<template>
  <v-app>
    <v-toolbar app dark >
        <v-toolbar-title class="headline text-uppercase">
          <span>Cartoon</span>
        </v-toolbar-title >
      <v-spacer></v-spacer>
        <v-btn href="/#/home" small ma0 flat>
          <span>Home</span>
        </v-btn>
        <v-btn href="/#/cartoon" small ma0 flat>
          <span>Cartoon</span>
        </v-btn>
        <v-btn href="/#/hello" small ma0 flat>
          <span>Contact us</span>
        </v-btn>
        <v-icon href="#" v-on:click="logout">exit_to_app</v-icon>
    </v-toolbar>
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
import firebase from 'firebase'
import Home from './components/Home'
import Vue from 'vue'
import Vuetify from 'vuetify'
 
Vue.use(Vuetify)
export default {
  name: 'App',
  data () {
    return {
      items: [
      'Home', 'Cartoon', 'Contact', 'Sign Out'
      ]
    }
  },
  methods: {
    logout: function () {
      firebase.auth().signOut().then(() => {
        this.$router.replace('login')
      })
    }
  }
}
</script>
