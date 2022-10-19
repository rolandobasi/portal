<template>
  <div>
    <nav>
      <v-toolbar
        src="@/assets/img/nabvarfondo.jpeg"
        app
        v-if="!$vuetify.breakpoint.sm && !$vuetify.breakpoint.xs"
      >
        <v-toolbar-title>Portal de Transparencia</v-toolbar-title>
        <v-btn color="#696969" dark text>
          <v-icon size="20">mdi-home</v-icon>
          Inicio
        </v-btn>
        <v-menu offset-y>
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="#696969" text dark v-bind="attrs" v-on="on">
              Información Oficiosa <v-icon>mdi-chevron-down</v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item>
              <v-list-item-title>Solicitud de Información</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>Informacion Oficiosa</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-btn text color="#696969">
          <v-icon>mdi-account-box</v-icon> Contactenos
        </v-btn>
        <v-spacer></v-spacer>

        <v-text-field dense placeholder="Buscar..." hide-details></v-text-field>
        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-toolbar>
      <v-toolbar src="@/assets/img/nabvarfondo.jpeg" app v-else>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-spacer></v-spacer>

        <v-text-field dense placeholder="Buscar..." hide-details></v-text-field>
        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-toolbar>
    </nav>
    <v-navigation-drawer
      src="@/assets/img/nabvarfondo.jpeg"
      app
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Inicio</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-group :value="true" prepend-icon="mdi-account-circle">
          <template v-slot:activator>
            <v-list-item-title>Informacion Oficiosa</v-list-item-title>
          </template>
          <v-list-item link class="mx-4">
            <v-list-item-icon>
              <v-icon>mdi-circle-box-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Solicitar Informacion</v-list-item-title>
          </v-list-item>
          <v-list-item link class="mx-4">
            <v-list-item-icon>
              <v-icon>mdi-circle-box-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Información Oficiosa</v-list-item-title>
          </v-list-item>
        </v-list-group>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-account-box</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Contactenos</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "NabVar",
  data() {
    return {
      drawer: false,
      items: [
        { title: "Inicio", icon: "mdi-home" },
        { title: "Información Oficiosa", icon: "mdi-folder-information" },
        { title: "Users", icon: "mdi-account-group-outline" },
      ],
      mini: true,
    };
  },
};
</script>

<style></style>
