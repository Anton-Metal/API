<template>
  <v-app>
    <div class="backgruond"></div>
  
	 
  
        
      
     
    
          <router-link to="/login">Home</router-link>
       
          <router-link to="/dashboard">dashboard</router-link>
      

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

import Login from './views/Login.vue'
export default {
  name: "App",
  components: {
    Login
  },

};
</script>
<style>
  .backgruond{
    background-image: url(./assets/skalman3.png) !important;
    height: 300px;
    width: 100%;
    display: block;
    position: absolute;
    top: 0;
    background-size: cover;
  }
</style>