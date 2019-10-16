
<template>
      <v-row   class="m-5">
  <CardDolar :dataProps="picker2" :callback="changeData"/>
  <v-card class="ml-5">
    <v-card-text>
    <h2>{{picker2}}</h2>
    </v-card-text>
  </v-card>
      </v-row>
</template>

<script>
//todo lo que se trabaje con Vuetify debe estar contenido en v-app
import CardDolar from "./CardDolar.vue";

export default {
  components:{
  CardDolar
  },
  name: 'DateContainer',
  data: () => ({    
    picker2: new Date().toISOString().substr(0, 10)
  }),
    methods: {
      changeData(data){
        this.picker2 = data
        console.log("my metodo",data);
        
      }
    },
};
</script>
