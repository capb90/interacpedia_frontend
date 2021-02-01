<template>
  <v-container>
    <v-row class="d-flex justify-space-between">
      <v-col max-height="150">
        <v-hover v-slot="{ hover }" light>
          <v-card
            :elevation="hover ? 4 : 2"
            class="mx-auto"
            height="400"
            max-width="350"
          >
            <v-container>
              <v-row class="d-flex justify-center mt-2">
                <v-icon size="60px" color="rgba(8,126,223,1)"
                  >mdi-cube</v-icon
                >
              </v-row>

              <v-row class="d-flex justify-center mt-5">
                <p class="font-weight-bold headline text--white">
                   Quienes somos 
                </p>
              </v-row>

              <v-row class="d-flex justify-center mt-2">
                <p class=" subtitle-1 text--white ma-3">
                   Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad quis eum vero minus officia nihil repudiandae autem ipsa ducimus quaerat, enim minima, asperiores quidem velit fuga. Neque magnam enim iure.
                </p>
              </v-row>
            </v-container>
          </v-card>
        </v-hover>
      </v-col>

      <v-col max-height="150">
        <v-hover v-slot="{ hover }" light>
          <v-card
            :elevation="hover ? 4 : 2"
            class="mx-auto"
            height="400"
            max-width="350"
          >
            <v-container>
              <v-row class="d-flex justify-center mt-2">
                <v-icon size="60px" color="rgba(8,126,223,1)"
                  >mdi-face-agent</v-icon
                >
              </v-row>

              <v-row class="d-flex justify-center mt-5">
                <p class="font-weight-bold headline text--white">
                  Nuestros servicios 
                </p>
              </v-row>

              <v-row class="d-flex justify-center mt-3">
                <p class=" subtitle-1 text--white ma-3">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore omnis incidunt, earum quod vero aspernatur ut recusandae iure adipisci dolores est, explicabo tempora eius deserunt error nemo eos quisquam libero! <br/>buscando la optimización de los servicios.
                </p>
              </v-row>
            </v-container>
          </v-card>
        </v-hover>
      </v-col>

      <v-col max-height="150">
        <v-hover v-slot="{ hover }" light>
          <v-card
            :elevation="hover ? 4 : 2"
            class="mx-auto"
            height="400"
            max-width="350"
          >
            <v-container>
              <v-row class="d-flex justify-center mt-2">
                <v-icon size="60px" color="rgba(8,126,223,1)"
                  >mdi-account-multiple-plus</v-icon
                >
              </v-row>

              <v-row class="d-flex justify-center mt-5">
                <p class="font-weight-bold headline text--white">
                  contactanos 
                </p>
              </v-row>

              <v-row class="d-flex justify-center mt-3">
                <p class=" subtitle-1 text--white ma-3">
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae doloribus, nesciunt porro suscipit minus amet error consequuntur! Similique neque nisi saepe, fugit hic architecto, beatae asperiores quibusdam magni ab dolore.  <br/> identificación de clientes potenciales
                </p>
              </v-row>
            </v-container>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>


<script>
export default {
  data() {
    return {};
  }
};
</script>