<template>
  <v-app>
    <v-app-bar color="transparent" style="backdrop-filter: blur(100px)" fixed>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>
        Georges AYENI
      </v-app-bar-title>
    </v-app-bar>
    <v-navigation-drawer scrim style="backdrop-filter: blur(100px)" color="transparent" v-model="drawer"></v-navigation-drawer>
    <v-main class="mt-n5">
      <router-view />
    </v-main>
    <v-footer color="transparent" style="backdrop-filter: blur(100px)" border elevation="10" height="100">
      <div>@Georges AYENI</div>
      <v-spacer></v-spacer>
      <v-btn class="mx-2" flat @click="link('https://github.com/Georges987')" icon="mdi-github" color="white"></v-btn>
      <v-btn class="mx-2" flat @click="link('https://facebook.com/georges.ayeni.7')" icon="mdi-facebook"
        color="white"></v-btn>
      <v-btn class="mx-2" flat @click="link('https://www.linkedin.com/in/georges-ayeni-542a461bb/')" icon="mdi-linkedin"
        color="white"></v-btn>
    </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false,
  }),

  methods: {
    link(url) {
      window.open(url, '_blank');
    }
  },
}
</script>