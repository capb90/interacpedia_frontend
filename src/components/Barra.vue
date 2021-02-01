<template>
  <v-card max-height="500" tile>
    <v-img
      src="https://blog.powerdata.es/hs-fs/hubfs/Stock%20images/cabecera%20modelos%20predictivos.jpg?width=1000&name=cabecera%20modelos%20predictivos.jpg"
      gradient="to right, rgba(8,126,223,.75), rgba(1,66,182,1)"
      max-height="500"
      dark
    >
      <v-container fluid>
        <v-row>
          <v-col cols="5">
            <p class="title text--white ml-8">
             Nombre de la empresa
            </p>
          </v-col>

          <v-col cols="6">
            <v-tabs
              class="d-flex justify-end"
              background-color="rgba(145,25,89,0)"
            >
              <!-- <v-tab><a href="#equipo">quienes somos</a></v-tab> -->
                       
              <v-tab><a href="#servicios"> servicios</a></v-tab>
              <!-- <v-tab><a href="#testimonios">testimonios</a></v-tab> -->
              <!-- <v-tab><a href="#equipo">equipo</a></v-tab> -->
            </v-tabs>
          </v-col>

          <v-col class="d-flex justify-center" cols="1">
            <v-btn icon :to="{ name: 'login' }">
              <v-icon>mdi-account</v-icon>
            </v-btn>
          </v-col>
        </v-row>

        <v-spacer class="pa-8"></v-spacer>

        <v-row>
          <v-col align="center"> </v-col>
        </v-row>

        <v-row class="pt-16">
          <v-col align="center">
            <p class="font-weight-bold display-2 text--white">
             Tecnologia<br />
            </p>
          
          </v-col>
        </v-row>
      </v-container>
    </v-img>
  </v-card>
</template>


<script>
export default {};
</script>