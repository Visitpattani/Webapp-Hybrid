<template>
    
    <div class="row">
      <div class="col m4">
        <div class="card">
          <div class="card-image">
            <img src="https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/13179432_1072810349458454_3014148935445179896_n.jpg?_nc_cat=101&oh=33b37e312424a3cda13f8943e734a860&oe=5C58D541"
            style="height:65vh"
            />
          </div>
          <div class="card-content">
            <h5><span class="left">Arm</span>Teetawat Riya <span class="right">5810110160</span></h5>
          </div>
        </div>
      </div>
      <div class="col m4">
        <div class="card">
          <div class="card-image">
            <img src="https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/482966_508036145892041_2143320946_n.jpg?_nc_cat=103&oh=16c79f0e2afb240ec5df9d74819ad316&oe=5C5D25E1"
            style="height:65vh;"
            />
          </div>
          <div class="card-content">
            <h5><span class="left">Toh</span>Chalerm Sae-wang <span class="right">5810110058</span></h5>
          </div>
        </div>
      </div>  
      <div class="col m4">
        <div class="card">
          <div class="card-image">
            <img src="https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/21766772_1474132312667117_8807724213492104882_n.jpg?_nc_cat=108&oh=f1186dc8171c87ed3f724c56d5ed3b04&oe=5C557410"
            style="height: 65vh"
            />
          </div>
          <div class="card-content">
            <h5><span class="left">Geng</span>Thanaphon Toprasit <span class="right">5810110451</span></h5>
          </div>
        </div>
      </div>
      <div class="col m4">
        <div class="card">
          <div class="card-image">
            <img src="https://scontent.fbkk14-1.fna.fbcdn.net/v/t1.0-9/17861859_1867803166765689_1497751698758696041_n.jpg?_nc_cat=106&_nc_ht=scontent.fbkk14-1.fna&oh=bc2642cf943e9ef3fa82b4059383e54d&oe=5CAA146D"
            style="height: 65vh"
            />
          </div>
          <div class="card-content">
            <h5><span class="left">Dear</span>Adinan Yujaroen <span class="right">5810110368</span></h5>
          </div>
        </div>
      </div>
      <div class="col m4">
        <div class="card">
          <div class="card-image">
            <img src="https://scontent.fbkk14-1.fna.fbcdn.net/v/t31.0-8/10835309_670534886390035_4066111135281035727_o.jpg?_nc_cat=104&_nc_ht=scontent.fbkk14-1.fna&oh=9bb8e06c065a273e3aa46151bbd1d403&oe=5CB14468" style="height: 65vh"/>
          </div>
          <div class="card-content">
            <h5><span class="left">Care</span>Surachok Hemadhulin <span class="right">5810110362</span></h5>
          </div>
        </div>
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
      msg: 'Welcome to Your Vue.js App'
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
