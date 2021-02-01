<template >
  <v-footer
    class="pt-10"
    height="250"
    dark
    padless
    color="rgba(1,66,182,1)"
    gradient="to right, rgba(8,126,223,1), rgba(1,66,182,1)"
  >
    <v-card
      class="flex"
      flat
      tile
      color="rgba(1,66,182,1)"
      gradient="to right, rgba(8,126,223,1), rgba(1,66,182,1)"
    >
      <v-card-title>
        <p class="body-1">Andrés Portillo: capb90@hotmail.com-Pasto</p>

        <v-spacer></v-spacer>

        <!-- <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
          <v-icon size="24px">
            {{ icon }} 
          </v-icon>
        </v-btn> -->
        <v-btn v-for="icon in icons" :key="icon" class="mx-3" icon>
          <a :href="icon.url" :target="icon.target"><v-icon size="24px">{{ icon.name }}</v-icon></a>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} —
        <strong>Software Development Team</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>


<script>
export default {
  data: () => ({
    icons: [
      {
        name: "mdi-github",
        url: "https://github.com/capb90",
        target: "_blank",
      },
    ],
  }),
};
</script>