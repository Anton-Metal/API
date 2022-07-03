<template>
  

    <v-main class="d-flex justify-center align-center">
      <v-col cols="10" lg="4" class="mx-auto">
        <v-card class="pa-4">
          <div class="text-center">
            <v-avatar size="100" color="indigo lighten-4">
              <v-icon size="40" color="indigo">mdi-account</v-icon>
            </v-avatar>
            <h2 class="indigo--text">Login Page</h2>
          </div>
          <v-form @submit.prevent="submitHandler" ref="form">
            <v-card-text>
              <v-text-field
               
                label="Email"
                placeholder="Email"
                prepend-inner-icon="mdi-account"
              />
              <v-text-field
                      label="Password"
                      placeholder="Password"
                      prepend-inner-icon="mdi-key"
                      :append-icon="passwordShow ? 'mdi-eye':'mdi-eye-off'"
                />
              
            </v-card-text>
            <v-card-actions class="justify-center">
  			<v-btn>
          	<router-link class="text-decoration-none" to="/dashboard">Login</router-link>
        	</v-btn>            
			</v-card-actions>
          </v-form>
        </v-card>
      </v-col>
    </v-main>
   

</template>

<script>

export default {
  name: 'Login',

 
};
</script>

