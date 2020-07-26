<template>
  <div>
     <v-container class="mt-5 mb-5">
        <v-row>
          <v-col
            md="10"
            offset-md="1"           
          >
            <p class="text-h5 font-weight-bold">Course <span class="amber--text text--darken-3">Available</span></p>
            <p class="text-caption" style="width:60%">Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime, temporibus aliquid id cumque </p>
          </v-col>
        </v-row>
        <v-row>
          <v-sheet
            class="mx-auto"
            elevation="0"
            style="width:100%;"
          >
            <v-slide-group
              v-model="slider"
              active-class="grey lighten-1"
              show-arrows
            >
              <v-slide-item
                v-for="(a_course, i) in a_courses"
                :key="i"
                v-slot:default="{ active, toggle }"
              >
                <v-card
                  color="grey lighten-3"
                  class="ma-4"
                  width="240"
                  @click="toggle"
                >
                  <v-img
                    class="white--text align-end"
                    height="180px"
                    :src= "require('../assets/courseAvailable/'+a_course.img)"
                  >
                    <v-card-title style="background-color:rgba(0,0,0,.5);" class="text-caption">
                      <v-icon left color="amber darken-3">
                        {{a_course.icon}}
                      </v-icon>
                      {{a_course.title}}
                    </v-card-title>
                  </v-img>

                  <!-- <v-card-subtitle class="pb-0">Number 10</v-card-subtitle> -->

                  <v-card-text class="text--primary text-justify">
                    {{a_course.desc}}
                  </v-card-text>
                    <v-divider light></v-divider>
                  <v-card-actions >
                    <v-row>
                      <v-col
                        md="12"
                      >
                          <span>
                            <v-icon left>
                              account_circle 
                            </v-icon>
                            {{a_course.member}}
                          </span>
                          <!-- <v-divider vertical light></v-divider> -->
                          <span class="mr-5">
                            <v-icon left right>
                              visibility
                            </v-icon>
                            {{a_course.view}}
                          </span>
                          <span>
                            <v-btn small color="amber darken-3 white--text" class="text-body-2">
                              $ {{a_course.price}}
                            </v-btn>
                          </span>
                      </v-col>
                    </v-row>
                  </v-card-actions>
                </v-card>
              </v-slide-item>
            </v-slide-group>
          </v-sheet>
        </v-row>
      </v-container>
  </div>
</template>
<script>
export default {
  name: "CourseAvailable",
  data(){
    return{
      slider: null,
      a_courses: [
        {
          title: 'Software Enginering',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'code',
          price: 233,
          img: 'Group 3.png',
          view: 28
        },
        {
          title: 'Cinematic Photo',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'photo_camera',
          price: 233,
          img: 'Group 4.png',
          view: 28
        },
        {
          title: 'Server Security',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'security',
          price: 233,
          img: 'Group 5.png',
          view: 28
        },
        {
          title: 'Software Enginering',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'code',
          price: 233,
          img: 'Group 3.png',
          view: 28
        },
        {
          title: 'Cinematic Photo',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'photo_camera',
          price: 233,
          img: 'Group 4.png',
          view: 28
        },
        {
          title: 'Server Security',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'security',
          price: 233,
          img: 'Group 5.png',
          view: 28
        },
        {
          title: 'Software Enginering',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'code',
          price: 233,
          img: 'Group 3.png',
          view: 28
        },
        {
          title: 'Cinematic Photo',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'photo_camera',
          price: 233,
          img: 'Group 4.png',
          view: 28
        },
        {
          title: 'Server Security',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit ducimus aperiam cupiditate in maxime',
          member: 100,
          icon: 'security',
          price: 233,
          img: 'Group 5.png',
          view: 28
        },
      ]
    }
  }
}
</script>