<template>
<div>
  <div class="row" v-for="user in users">
    <div class="col m2"></div>
    <div class="col m8 card" style="padding:20px">
      <div class="row">
        <div class="col s12 m4 center">
          <img :src="user.pic" class="circle" style="width:200px; height:200px">
        </div>
        <div class="col s12 hidden-md-and-up center">
          <h5>{{user.name}}</h5>
          <h5 >{{user.id}}</h5>
          <hr  style="border: 2px solid steelblue;">
          <h5>{{user.job}}</h5>
        </div>
        <div class="col m8 hidden-sm-and-down" style="padding-right:50px; padding-top:10px">
          <h3>{{user.name}} <span class="right">{{user.id}}</span></h3>
          <hr  style="border: 2px solid steelblue;">
          <h5 class="center">{{user.job}}</h5>
        </div>
      </div>
    </div>
    <div class="col m2"></div>
  </div>
</div> 
</template>

<script>
import firebase from 'firebase'
import GoogleMap from './GoogleMap'
export default {
  name: 'HelloWorld',
  data: function() {
    return {
      msg: 'Welcome to Your Vue.js App',
      users: [
        {name:"Teetawat Riya", id:"5810110160", job:"cordova + github developer", pic:"https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/13179432_1072810349458454_3014148935445179896_n.jpg?_nc_cat=101&oh=33b37e312424a3cda13f8943e734a860&oe=5C58D541"},
        {name:"Chalerm Sae-wang", id:"5810110058", job:"Team Leader : Tello", pic:"https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/482966_508036145892041_2143320946_n.jpg?_nc_cat=103&oh=16c79f0e2afb240ec5df9d74819ad316&oe=5C5D25E1"},
        {name:"Thanaphon Toprasit", id:"5810110451", job:"UX designer & UI developer", pic:"https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/21766772_1474132312667117_8807724213492104882_n.jpg?_nc_cat=108&oh=f1186dc8171c87ed3f724c56d5ed3b04&oe=5C557410"},
        {name:"Adinan Yujaroen", id:"5810110368", job:"Database Developer", pic:"https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/17861859_1867803166765689_1497751698758696041_n.jpg?_nc_cat=106&_nc_ht=scontent.fbkk14-1.fna&oh=bc2642cf943e9ef3fa82b4059383e54d&oe=5CAA146D"},
        {name:"Surachok Hemadhulin", id:"5810110362", job:"UI developer", pic:"https://scontent.fbkk14-1.fna.fbcdn.net/v/t31.0-8/10835309_670534886390035_4066111135281035727_o.jpg?_nc_cat=104&_nc_ht=scontent.fbkk14-1.fna&oh=9bb8e06c065a273e3aa46151bbd1d403&oe=5CB14468"},
      ]
    }
  },
  methods: {
    logout: function () {
      firebase.auth().signOut().then(() => {
        this.$router.replace('login')
      })
    }
  },
  components: {
    'GoogleMap': GoogleMap,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  background-color: aliceblue;
  height: 100vh;
}
.menu:hover{
  color: white;
}
.active a{
  font-weight: bold;
}
a{
  font-size: 30px;
}
</style>
