<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="$vuetify.breakpoint.lgAndUp"
      app
    >
      <v-list dense>
        <template>
          <v-list-item :to="{ name: 'home' }">
            <v-list-item-action>
              <v-icon>home</v-icon>
            </v-list-item-action>
            <v-list-item-title> Inicio </v-list-item-title>
          </v-list-item>
        </template>

        <template>
          <v-list-group
            v-if="verificar === 'Administrador' || verificar === 'Almacenero'"
          >
            <v-list-item slot="activator">
              <v-list-item-content>
                <v-list-item-title> Almacén </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: 'categoria' }">
              <v-list-item-action>
                <v-icon>table_chart</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title> Categorías </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: 'articulo' }">
              <v-list-item-action>
                <v-icon>table_chart</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title> Servicios </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>

          <v-list-group v-if="verificar === 'Administrador'">
            <v-list-item slot="activator">
              <v-list-item-content>
                <v-list-item-title> Accesos </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: 'usuario' }">
              <v-list-item-action>
                <v-icon>table_chart</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title> Empleados </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="silver darken-3"
      dark
    >
      <v-toolbar-title style="width: 300px" class="ml-0 pl-3">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <span class="hidden-sm-and-down">Sistema</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn @click="salir()" icon> <v-icon>logout</v-icon> Salir </v-btn>

      <!-- <v-btn :to="{ name: 'login' }" icon v-else>
          <v-icon>apps</v-icon> Login
        </v-btn> -->
    </v-app-bar>

    <v-content>
      <v-container fluid fill-height>
        <v-slide-y-transition mode="out-in">
          <router-view />
        </v-slide-y-transition>
      </v-container>
    </v-content>
    <v-footer height="auto">
      <v-layout justify-center>
        <v-flex text-xs-center>
          <v-card flat tile color="primary" class="white--text">
            <v-card-text class="white--text pt-0">
              Proyecto final &copy;2020
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false
    };
  },
  computed: {
    verificar() {
      console.log(this.$store.state.usuario.rol);
      return this.$store.state.usuario.rol;
    }
  },
  methods: {
    salir() {
      this.$store.dispatch("salir");
    }
  }
};
</script>
