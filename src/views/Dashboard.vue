
<template>
  <div class="Dashboard">
   <v-container>
	<v-layout row wrap>
		<v-flex xs12 md12 >
			<DashboardComp/>
		</v-flex>

	</v-layout>
		   
      
	</v-container>

  </div>
</template>

<script>

import DashboardComp from '@/components/DashboardComp.vue'
export default {
  components: { DashboardComp },
 
  

}
</script>

<style>
body{
  color: white;
}

</style>