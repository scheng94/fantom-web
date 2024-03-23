<template>
  <v-app>
    <v-toolbar :elevation="8">
      <v-toolbar-title>
        <router-link to="/home" slots="span" style="cursor: pointer">
          <v-img :src="homeImage" height="70px"></v-img>
        </router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn
          flat
          v-for="item in menuItems"
          :key="item.title"
          :to="item.path">
          <v-icon left dark>{{ item.icon }}</v-icon>
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
    
    <v-content>
      <router-view></router-view>
    </v-content>

    <v-footer class="pa-0 footer">
      <div class="bg-blue-grey-darken-2 d-flex w-100 align-center px-4">
        <strong>Follow Us:</strong>
        <v-btn
          v-for="icon in footerIcons"
          :key="icon"
          :icon="icon"
          class="mx-4"
          size="small"
          variant="plain"
        ></v-btn>
        <v-spacer></v-spacer>
        <strong >&copy; {{ new Date().getFullYear() }} Fantom Corporation</strong>
      </div>

    </v-footer>
  </v-app>
</template>

<script>
  export default {
    name: "FantomApp",
    data(){
      return {
        homeImage: require('@/assets/FC_Logo_Transparent_White.png'),
        sidebar: false,
        menuItems: [
            { title: 'Home', path: '/home', icon: 'home' },
            { title: 'About', path: '/about', icon: 'about' },
            { title: 'Benefits', path: '/benefits', icon: 'benefits' },
            { title: 'Contact Us', path: '/contact-us', icon: 'contact-us' }
        ],
        footerIcons: [
          'mdi-facebook',
          'mdi-twitter',
          'mdi-linkedin',
          'mdi-instagram',
        ],
      }
    },
  };
</script>

<style>

.home-logo {
  max-width: 100%; /* Adjust the max-width as needed */
  height: 70px;
}

.footer {
  bottom: 0;
}
</style>