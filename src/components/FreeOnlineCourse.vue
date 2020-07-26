<template>
  <div>
      <v-row class="mt-5 mb-5">
        <v-col
          class="freeCourseLeft white--text"
          md="6"
        >
          <v-container class="mt-5">
            <v-row>
              <v-col
                md="10"
                offset-md="1"
              >
                <div class="text-h5 font-weight-bold">Online Course For Free</div>
                <div class="text-caption">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate assumenda ducimus rerum praesentium commodi facilis ad c</div>
                <v-form v-model="formValid">
                  <v-container>
                    <v-row>
                      <v-col
                        md="6"
                      >
                        <v-text-field
                          label="Your Name"
                          v-model="student.name"
                          required
                          :rules="studentNameRules"
                          dark
                        >

                        </v-text-field>
                        <v-text-field
                          label="Contact Number"
                          v-model="student.contact"
                          required
                          :rules="studentContactRules"
                          dark
                        >

                        </v-text-field>
                      </v-col>
                      <v-col
                        md="6"
                      >
                        <v-text-field
                          label="Your Email"
                          v-model="student.email"
                          required
                          :rules="studentEmailRules"
                          dark
                        >
                        </v-text-field>
                        <v-select
                          v-model="student.genre"
                          :items="genreOption"
                          label="Genre"
                          required
                          dark
                        ></v-select>
                      </v-col>
                      <v-col md="12" class="text-center">
                        <v-btn color="amber darken-3 white--text">Send Request</v-btn>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-form>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
        <v-col
          md="6"
          class="freeCourseRight"
        >
          <v-container class="mt-5">
            <v-row>
              <v-col
                md="10"
                offset-md="1"
              >
                <div class="text-h6 text-center">Next Set Of Free Online Course</div>
                <div class="text-h5 text-center font-weight-bold white--text text-uppercase">Launching Soon</div>
                <v-row style="margin-top:50px;">
                  <v-col
                    v-for="(time, i) in launchingTime"
                    :key="i"
                    md="3"
                  >
                    <v-row>
                      <v-col
                        md="10"
                        offset-md="1"
                        class="rounded text-center"
                        style="border:1px solid white"
                      >
                        <div class="text-h4 font-weight-bold">{{time.one}}</div>
                        <div class="text-h6 white--text">{{time.two}}</div>
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
  </div>
</template>
<script>
export default {
  name:'freeonlinecourse',
  data(){
    return{
      launchingTime: [
        {one: 2, two: 'Months'},
        {one: 28, two: 'Days'},
        {one: 14, two: 'Hours'},
        {one: 20, two: 'Minutes'},
      ],
      student: {
        name:'',
        email:'',
        contact:'',
        genre:''
      },
      genreOption:[
        'Male',
        'Female'
      ],
      studentNameRules:[],
      studentEmailRules:[],
      studentContactRules:[],
      studentGenreRules:[],
      formValid:false
    }
  }
}
</script>
<style scoped>
  .freeCourseRight{
    background-image:url('../assets/courseFree/Group 7.png');
    background-size:cover;
  }
  .freeCourseLeft{
    background-image:url('../assets/courseFree/Group 6.png');
    background-size:cover;
  }
</style>