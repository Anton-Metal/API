<template>
<div class="team">
<h1 class="display-2 my-7 white--text">Dashboard</h1>

<v-row >
  <v-col cols="12" sm="6" md="4" lg="3" v-for="item in list" v-bind:key="item.id">
	   <v-hover
          v-slot="{ hover }"
          
        >
	<v-card
	height="100%"
	:elevation="hover ? 4 : 2"
    class="mx-auto"
    max-width="344"
  	>
    <v-img
      :src="item.thumbnail"
      height="200px"
      cover
    ></v-img>



    <v-card-title>
      {{item.title}}
    </v-card-title>

    <v-card-text class="black--text">
     {{item.price}}
    </v-card-text>

	
	 
	<v-btn 
	class="blue white--text text-center ma-3"
	color="orange-lighten-2"
	variant="text"
	>
	Add to Cart
	</v-btn>    


   
  </v-card>
  </v-hover>
</v-col>
 
</v-row>
	

		
</div>
</template>
<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';

Vue.use(VueAxios,axios)

export default {
	name: "DashboardComp",
	data() {
		return {list: undefined} 
		
	},
	mounted() 
	{
		Vue.axios.get('https://dummyjson.com/products')
		.then((res)=> {
			this.list=res.data.products
			console.log(res.data.products)
		})
	}
}
</script>

 