  
  <template>
  <!-- <v-container fluid> -->
  <v-layout mt-2 mb-4 fluid>
    <v-flex>
      <v-carousel height="650px">
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
          gradient="to right, rgba(8,126,223,.5), rgba(1,66,182,.9)"
        >
          <v-spacer class="pa-16"></v-spacer>

          <v-container mt-14>
            <v-row class="d-flex justify-center mt-5">
              <v-col cols="6" align="center">
                <p class="font-weight-bold display-2 text--white">
                  Nombre de la empresa
                </p>
              </v-col>
            </v-row>

          </v-container>
        </v-carousel-item>
      </v-carousel>
    </v-flex>
  </v-layout>
  <!-- </v-container> -->
</template>



<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://www.neocheck.es/wp-content/uploads/2019/03/machine-learning.jpg"
        },
        {
          src: "https://www.securityroundtable.org/wp-content/uploads/2019/06/machine-learning.png"
        },
        {
          src: "https://s32519.pcdn.co/es/wp-content/uploads/sites/3/2020/08/machine-learning-webinar-recap-blog-hero-image-1536x649.jpg.webp"
        },
        {
          src: "https://www.ealde.es/wp-content/uploads/2018/04/gestion-de-riesgos-credito-modelo-predictivo.jpg"
        }
      ]
    };
  }
};
</script>