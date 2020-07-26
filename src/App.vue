<template>
  <v-app>
    <Navbar/>
    <v-main>
      <Banner/>
      <CourseAvailable/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import Banner from './components/Banner'
import CourseAvailable from './components/CourseAvailable'

export default {
  name: 'App',

  components: {
    Navbar,
    Banner,
    CourseAvailable
  },

  data: () => ({
    //
  }),
};
</script>
