<template>
<div id="equipo">
  <v-container my-10>
    <v-row class="d-flex justify-center mb-10" align="center">
      <p class="font-weight-bold display-2 text--white">Nuestro equipo</p>
    </v-row>

    <v-row class="d-flex justify-center mb-10" align="center">
      <p class="headline" style="text-align: center">
        PredicSystem pone a su disposición a un equipo humano que cuenta con alta cualificación y experiencia.
      </p>
    </v-row>

    <v-row>
      <v-col cols="12" sm="6" offset-sm="3">
        <v-card>
          <v-list two-line>
            <template v-for="(item, index) in items.slice(0, 6)">
              <v-subheader v-if="item.header" :key="item.header">
                {{ item.header }}
              </v-subheader>
              <v-divider
                v-else-if="item.divider"
                :key="index"
                :inset="item.inset"
              ></v-divider>
              <v-list-item v-else :key="item.title">
                <v-list-item-avatar>
                  <img :src="item.avatar" />
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title v-html="item.title"></v-list-item-title>
                  <v-list-item-subtitle
                    v-html="item.subtitle"
                  ></v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </template>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</div>
</template>


<script>
export default {
  data: () => ({
    items: [
      { header: "Equipo" },
      {
        avatar: "https://i.ibb.co/pyZ0FNB/pp.jpg",
        title: "Desarrollador Frontend",
        subtitle: `<span class="font-weight-bold">Javier Triana</span> &mdash; Ingeniero civil, egresado de la universidad distrital F.J.C`
      },
      { divider: true, inset: true },
      {
        avatar: "https://i.ibb.co/Z2bS9xY/pp-2.jpg",
        title: 'Desarrollador Tester',
        subtitle: `<span class="font-weight-bold">Gabriel Ardila</span> &mdash; Ingeniero Electrónico, egresado de la universidad javeriana`
      },
      { divider: true, inset: true },
      {
        avatar: "https://i.ibb.co/VHjGPKY/pp-1.jpg",
        title: "Desarrollador Backend",
        subtitle:
          '<span class="font-weight-bold">Andrés Portillo</span> &mdash; Ingeniero Electrónico, egresado de la universidad de Nariño'
      }
    ]
  })
};
</script>