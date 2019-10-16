<template >
    <div>
    <v-card class="mr-5" color="pink">      
      <v-date-picker v-model="picker2" color="green lighten-1 " header-color="primary"
      locale="es"
      :min="min" 
      :max="max"
      :change="getApiDay(picker2)"     
      full-width
      />
      <v-card-text  class="text-center">
      <h2> Valor del Dolar: <span
      v-if="bool">{{valor}}$</span>
      <span
      v-else>{{sms}}</span>
      </h2>
      
      </v-card-text>
      </v-card>    
        
    </div>
</template>

<script>
//todo lo que se trabaje con Vuetify debe estar contenido en v-app
import axios  from "axios";

export default {
  name: 'CardDolar',
  data: () => ({    
    picker2:new Date().toISOString().substr(0, 10),
    min:"1984-12-15",
    max:new Date().toISOString().substr(0, 10),    
    valor:"",
    bool:false,
    sms:"No hay valores disponibles para esta fecha"
  }),
    props: {
        dataProps:String, 
        callback:Function
    },
  methods: {  
      async getApiDay(date){          
          this.callback(this.picker2)          
        const endPoint=date.split("-").reverse().join("-")
        const data = await axios("https://mindicador.cl/api/dolar/"+endPoint)
                            .then(res=>res.data.serie[0])
                            if(data !=undefined){
                            this.valor= data.valor
                            this.bool=true;
                            }
                            else(
                              //this.valor= "Precio no disponible"
                              this.bool=false
                            )                            
      },
      
    },
    computed: {
       compare:()=>{
          return this.picker2 = this.dataProps
      }
    }
};
</script>