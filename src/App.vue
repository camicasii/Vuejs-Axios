
<template>
  <v-app >
    
    
    
    <Navbar :drawerNav="sidebarState"/> 
    
      <v-content class="contenido" >
      <SideBar :drawer="sidebarProps" :A="drawerApp"/>
      <v-container
      class="hijo"
        >      
      <router-view relative />
      </v-container>
      </v-content>      
    <Footer/>
  </v-app>
  
</template>

<script>
//todo lo que se trabaje con Vuetify debe estar contenido en v-app

import Navbar from "./components/Navbar.vue";
import SideBar from "./components/SideBar.vue";
import Footer from "./components/Footer.vue";

export default {
  components:{
    SideBar,
    Navbar,
    Footer
  },
  name: 'App',
  data(){
    return{drawerApp:true}
    
  },
  methods: {
    sidebarState(){      
      this.drawerApp = !this.drawerApp
      console.log(this.drawerApp);
      return this.drawerApp
    },
    sidebarProps(data){      
      //
    }

  },
    
};
</script>
