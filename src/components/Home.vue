<template>
  <v-content>
    <v-container>
      <h1> Welcome </h1>
      <h4>{{user.email}}</h4>
    </v-container>
  </v-content>
</template>

<script>
import firebase from 'firebase'
export default {
  name: 'Home',
  data: function() {
    return {
      msg: 'Welcome to Your Vue.js App',
      user: firebase.auth().currentUser
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
