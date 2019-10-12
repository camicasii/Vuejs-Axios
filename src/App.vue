
<template>
  <v-app>
    <v-content>
      <v-container>
      {{picker}} and {{picker2}} and
      {{max}}
      <v-row   class="m-5">
      <v-card class="mr-5">      
      <v-date-picker v-model="picker2" color="green lighten-1 " header-color="primary"
      locale="es"
      :min="min"      
      ></v-date-picker>
      </v-card>    
      <v-card>
      <v-date-picker v-model="picker" color="green lighten-1 "></v-date-picker>
      
      </v-card>    
      <v-card
    class="mx-auto"
    max-width="400"   
  >
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Top 10 Australian beaches</v-card-title>
    </v-img>



    <v-card-text class="text--primary">
      <div>Whitehaven Beach</div>

      <div>Whitsunday Island, Whitsunday Islands</div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="orange"
        text
      >
        Share
      </v-btn>

      <v-btn
        color="orange"
        text
      >
        Explore
      </v-btn>
    </v-card-actions>
  </v-card>
      
      
      </v-row>
      </v-container>



      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
//todo lo que se trabaje con Vuetify debe estar contenido en v-app
import axios  from "axios";

export default {
  name: 'App',
  data: () => ({
    picker: new Date().toISOString().substr(0, 10),
    picker2: new Date().toISOString().substr(0, 10),
    min:"1984-12-15",
    max:"2019-12-15",
    date: '2018-03-02'
  }), methods: {
      allowedDates: val => parseInt(val.split('-')[2], 10) % 2 === 0,
      async getApi(){
        const data = await axios("https://mindicador.cl/api/dolar")
                            .then(res=>res.data)
        console.log(data);
          
        
      }
    },
    created() {
      this.getApi()
    },
  
    
  
};
</script>
