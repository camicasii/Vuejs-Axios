<template>
<div>
   <v-toolbar >

      <v-app-bar-nav-icon ></v-app-bar-nav-icon>



      <v-toolbar-title >Title</v-toolbar-title>

      <div class="flex-grow-1">
      <v-btn text><router-link class="nav-item mx-3" to="/botones" exact>Botones</router-link></v-btn>
      </div>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon @click="drawerNav">
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>


        
    
    
    </div>
</template>

<script>

export default {
  
    name:'Navbar',
    props:{
      drawerNav:Function
    }, methods: {
      casa:()=>{
        console.log("hola")
      }
    },
}
</script>