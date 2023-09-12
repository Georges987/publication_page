<template>
  <v-carousel height="100vh" cycle :progress="true">
    <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover reverse-transition="fade-transition"
      transition="fade-transition">
      <v-sheet color="transparent" class="fill-height ma-0">
        <v-row class="fill-height" align="center" justify="center">
          <div class="text-h3 text-white font-weight-bold">{{ item.text }}</div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>

  <v-container class="text-center my-10">
    Bienvenue sur ma page de publication.
    Ici, vous trouverez la plupart de mes créations et pourrai y accéder gratuitement.
    N'hésitez pas à m'envoyer un mail où à tout simplement me contacter dès que vous
    ressentirez la nécessité. Encore Bienvenue.
  </v-container>
  <v-divider inset color="primary" length="500"></v-divider>

  <v-container class="my-16">
    <v-card elevation="15">
      <v-img aspect-ratio="1/2" cover height="500" src="/images/sqflite.png"></v-img>
      <v-card-title>
        Exemple test with sqflite and flutter framework
      </v-card-title>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn prepend-icon="mdi-github" @click="download('https://github.com/Georges987/flutter_sqflite_student')">
          Git
        </v-btn>
        <v-btn prepend-icon="mdi-download" @click="download('/files/sqflite-student.apk')">
          Télécharger l'APK
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
