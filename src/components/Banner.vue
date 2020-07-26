<template>
  <div>
      <v-parallax
        height="700"
        class="mb-5"
        src="../assets/banner/Mask Group 1.png"
      >
        <v-container>
          <v-row>
            <v-col
              xs="10"
              offset-xs="1"
              sm="10"
              offset-sm="1"
              md="10"
              offset-md="1"
              class="white--text"
            >
              <p class="text-h4 text-uppercase font-weight-bold">We are engage to give you</p>
              <p class="text-h3 text-uppercase amber--text text--darken-3 font-weight-bold" >A good future</p>
              <p class="text-caption" style="width:60%">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam dolore quaerat, culpa mollitia temporibus rem voluptates neque ab eaque earum sunt eum, vitae</p>
              <v-btn color="amber darken-3">Purchase</v-btn>
              <v-btn color="white" outlined class="ml-3">Learn More</v-btn>
            </v-col>
          </v-row>
          <!-- <v-row style="margin-top:200px">
            <v-col
              md="10"
              offset-md="1"
            >
              <v-row>
                <v-col
                  md="4"
                  v-for="k_course in k_courses"
                  :key="k_course.name"
                  :class="k_course.bg"
                >
                  <p class="text-h5">
                    <v-row>
                      <v-col md="3">
                        <v-icon
                          x-large
                          class="mt-2"
                        >
                          {{k_course.icon}}
                        </v-icon>
                      </v-col>
                      <v-col md="9">
                        {{k_course.name}}
                      </v-col>
                    </v-row>
                  </p>
                  <p class="text-caption">
                    {{k_course.desc}}
                  </p> 
                </v-col>
              </v-row>

            </v-col>
          </v-row> -->
        </v-container>

      </v-parallax>
  </div>
</template>
<script>
export default {
  name: 'Banner',
  data(){
    return{
      k_courses:[
        {
          name:'Highly Qualified Teacher',
          desc:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam dolore quaerat',
          icon:'menu_book',
          bg:'grey lighten-1'
        },
        {
          name:'World Class Teaching',
          desc:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam dolore quaerat',
          icon:'emoji_events',
          bg:'amber darken-3'
        },
        {
          name:'International Syllabus',
          desc:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam dolore quaerat',
          icon:'insert_chart',
          bg:'grey lighten-1'
        },
      ]
    }
  }
}
</script>
<style scoped>
  
</style>