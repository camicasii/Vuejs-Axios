<template>
         <v-container fluid class="pa-0" 
         >
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <v-btn x-small color="secondary" dark>Extra small Button</v-btn>
          </div>
          <div class="my-2">
            <v-btn small color="primary" dark>Small Button</v-btn>
          </div>
          <div class="my-2">
            <v-btn color="warning" dark>Normal Button</v-btn>
          </div>
          <div class="my-2">
            <v-btn color="error" dark large>Large Button</v-btn>
          </div>
          <div class="my-2">
            <v-btn x-large color="success" dark>Extra large Button</v-btn>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <v-btn color="secondary" fab x-small dark>
              <v-icon>mdi-television</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="primary" fab small dark>
              <v-icon>mdi-pencil</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="warning" fab dark>
              <v-icon>mdi-account-circle</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="error" fab large dark>
              <v-icon>mdi-alarm</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="success" fab x-large dark>
              <v-icon>mdi-domain</v-icon>
            </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
    <div class="my-2">
        <v-btn text small color="primary">Primary</v-btn>
      </div>
       <div class="text-center">
    <v-btn class="ma-2" outlined color="indigo">Outlined Button</v-btn>
    <v-btn class="ma-2" outlined fab color="teal">
      <v-icon>mdi-format-list-bulleted-square</v-icon>
    </v-btn>
    <v-btn class="ma-5" outlined large fab color="indigo">
      <v-icon>mdi-pencil</v-icon>      
    </v-btn>    
    <v-btn class="ma-2" outlined large fab color="green">
    <v-icon>fingerprint</v-icon>
    </v-btn>
  </div>
   <v-btn block color="secondary" dark>Block Button</v-btn>
  </v-container>



    
</template>

<script>
export default {
    name:'Botones'
}
</script>