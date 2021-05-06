<template>
  <v-container>
   <v-toolbar flat>
  <img class="navbar-logo" src="../assets/images/img50.png" alt="Nordicpixel LOGO">
     

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-xs-only">
          <v-btn text>
            <router-link to="/">Forside</router-link>
          </v-btn>

          <v-btn text>
            <router-link to="/about">Hvem er HK</router-link>
          </v-btn>

          <v-btn text>
            <router-link to="/contact">Kontakt mig</router-link>
          </v-btn>
      </v-toolbar-items>
      <div class="hidden-sm-and-up">
        <div class="text-center">
    <v-menu offset-y>
      <template v-slot:activator="{ on }">
           <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
      </template>
      <v-list class="responsiveMenu">
      <v-list-item>
              <v-list-item-title><router-link to="/">Home</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/about">About</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/contact">Contact</router-link></v-list-item-title>
            </v-list-item>
      </v-list>
    </v-menu>
  </div>
      </div>
    </v-toolbar>
  </v-container>
</template>

<script>
  export default {
    name: 'Header',

    data: () => ({

    }),
  }
</script>

<style scoped>
.navbar-logo {
  width: 230px;
  height: auto;
}
</style>