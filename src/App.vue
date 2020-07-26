<template>
  <v-app>
    <Navbar/>
    <v-main>
      <Banner/>
      <CourseAvailable/>
      <FreeOnlineCourse/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import Banner from './components/Banner'
import CourseAvailable from './components/CourseAvailable'
import FreeOnlineCourse from './components/FreeOnlineCourse'

export default {
  name: 'App',

  components: {
    Navbar,
    Banner,
    CourseAvailable,
    FreeOnlineCourse
  },

  data: () => ({
    //
  }),
};
</script>
