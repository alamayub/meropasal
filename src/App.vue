<template>
  <v-app>
    <Navbar />

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue'
export default {
  name: 'App',
  components: { Navbar },
  data: () => ({  }),
}
</script>

<style>
.container {
  max-width: 1450px !important;
  margin-right: auto !important;
  margin-left: auto !important;
  padding: 12px !important;
}

/* Image */
img {
  display: block;
  height: 100%;
  width: 100%;
  object-fit: contain;
}
</style>