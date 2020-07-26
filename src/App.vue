<template>
  <v-app>
    <Navbar/>
    <v-main>
      <Banner/>
      <CourseAvailable/>
      <FreeOnlineCourse/>
      <Encourage/>
      <CountProduct/>
      <RecentRelase/>
      <Partnership/>
      <UpcomingEvent/>
      <Feedback/>
      <News/>
      <JobInviteVue/>
      <FooterVue/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import Banner from './components/Banner'
import CourseAvailable from './components/CourseAvailable'
import FreeOnlineCourse from './components/FreeOnlineCourse'
import Encourage from './components/Encourage'
import CountProduct from './components/CountProduct'
import RecentRelase from './components/RecentRelase'
import Partnership from './components/Partnership'
import UpcomingEvent from './components/UpcomingEvent'
import Feedback from './components/Feedback'
import News from './components/News'
import JobInviteVue from './components/JobInvite.vue'
import FooterVue from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    Banner,
    CourseAvailable,
    FreeOnlineCourse,
    Encourage,
    CountProduct,
    RecentRelase,
    Partnership,
    UpcomingEvent,
    Feedback,
    News,
    JobInviteVue,
    FooterVue
  },

  data: () => ({
    //
  }),
};
</script>
