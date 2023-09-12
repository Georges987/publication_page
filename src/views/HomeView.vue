<template>
      <v-carousel height="100vh" cycle :progress="true">
        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover reverse-transition="fade-transition"
          transition="fade-transition">
          <v-sheet color="transparent" class="fill-height ma-0">
            <v-row class="fill-height" align="center" justify="center">
              <div class="display-3">{{ item.text }}</div>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>

      <v-container class="my-16">
        <v-card>
          <v-img src="/images/sqflite.png"></v-img>
          <v-card-title>
            Exemple test with sqflite and flutter framework
          </v-card-title>
          <v-card-actions>
            <v-btn append-icon="mdi-github" @click="download('https://github.com/Georges987/flutter_sqflite_student')">
              Accéder au repositorie Git
            </v-btn>
            <v-btn append-icon="mdi-download" @click="download('/files/sqflite-student.apk')">
              Télécharger l'application
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-container>
</template>

<script>

export default
  {
    name: 'HomeView',
    methods:
      {
        download(url) {
          window.open(url, '_blank');
        },
      },

    data: () => ({
      publications: [
        {
          src: '/images/banner.png',
          description: 'Bienvenue',
          images: [
            '/images/banner.png',
            '/images/banner.png',
            '/images/banner.png',
            '/images/banner.png',
          ],
          file: 'https://www.youtube.com/watch?v=5qap5aO4i9A',
        },
      ],
      items: [
        {
          src: '/images/banner.png',
          text: 'Bienvenue',
        },
      ],
    }),
  };
</script>
