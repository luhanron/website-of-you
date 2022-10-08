<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      flat
    >
    <HelloWorld/>
    </v-app-bar>

    <v-main>
      <GalleryVue/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import GalleryVue from './components/GalleryVue';

export default {
  name: 'App',

  components: {
    HelloWorld,
    GalleryVue
  },

  data: () => ({
    //
  }),
};
</script>
