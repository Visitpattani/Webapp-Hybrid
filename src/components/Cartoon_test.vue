<template>

  <v-layout>
    <v-flex xs12 sm6 offset-sm3>
      <h1 class="text-xs-center">Cartoon</h1>
    <v-carousel height="auto" hide-delimiters>
      <v-carousel-item v-for="(location, idx) in locations" :key="idx" :src="location.url"/>
    </v-carousel>
    </v-flex>
  </v-layout>
</template>

<script>
import firebase from 'firebase'
import { db } from '../main'
import { compare } from 'semver';
export default {
  name: 'Cartoon_test',
  data: function() {
    return {
        locations: [],
        msg: 'Welcome to Your Vue.js App',
        user: firebase.auth().currentUser
    }
  },
  firestore () {
    return {
      locations: db.collection("cartoon")
                   .orderBy("name", "asc")
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h5 {
  font-weight: normal;
}
.block {
  border: white 2px solid; 
}
.menu:hover{
  color: white;
}
a{
  font-size: 30px;
}
.active a{
  font-weight: bold;
}
</style>
