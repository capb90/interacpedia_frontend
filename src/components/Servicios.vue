<template>
<div id="servicios">
  <v-container my-16>
    <v-row class="d-flex justify-center mb-9" align="center">
      <p class="font-weight-bold display-2 text--white">Nuestros Servicios</p>
    </v-row>


    <v-row>
      <v-col v-for="(art, indice) of datos" :key="art.id">
        <v-card
          class="col-lg-6 col-xs-12 border"
          max-width="344"
          v-if="indice <= 2"
        >
          <v-img :src="art.codigo" height="200px"></v-img>

          <v-card-title> {{ art.nombre }} </v-card-title>

          <v-card-subtitle> {{ art.descripcion }} </v-card-subtitle>

          <v-card-actions>
            <v-btn target= '_blank' href="https://www.sas.com/es_co/insights/big-data/what-is-big-data.html" color="orange lighten-2" text>Leer</v-btn>

            <v-spacer></v-spacer>

            <v-btn icon @click="show = !show">
              <v-icon>{{
                show ? "mdi-chevron-up" : "mdi-chevron-down"
              }}</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</div>
</template>




<script>
import axios from "axios";
export default {
  data() {
    return {
      datos: null
    };
  },
  mounted() {
    axios.get("articulo/list").then(response => (this.datos = response.data));
  }
};
</script>