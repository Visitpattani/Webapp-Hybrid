<template>
  <v-content>
    <v-container>
      <img id="logo" src="@/assets/overview.png"/>
      <h1 class="hidden-sm-and-down">แอปพลิเคชั่นอ่านการ์ตูนอันดับ 1 ของคนไทย</h1>
      <h5 class="hidden-md-and-up center">แอปพลิเคชั่นอ่านการ์ตูน</h5>
      <h5 class="hidden-md-and-up center">อันดับ 1ของคนไทย</h5>
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
