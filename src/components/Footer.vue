<template>
  <div>
    <v-container fluid class="bg-footer">
      <v-container class="mt-5 mb-5">
        <v-row>
          <v-col md="10" offset-md="1">
            <v-row>
              <v-col md="3">
                <v-row>
                  <v-col md="3">
                    <v-img height="50" contain src="../assets/navbarIcon/e-learning.png"></v-img>
                  </v-col>
                  <v-col md="8">
                    <div class="text-h6 white--text mt-2">Atrem Educate</div>
                  </v-col>
                  <div class="grey--text mini-text mb-3">Lorem ipsum dolor sit amet dolor sit </div>

                  <v-col md="3">
                    <v-btn small outlined color="grey">
                      <v-icon small>
                        call
                      </v-icon>
                    </v-btn>
                  </v-col>
                  <v-col md="8">
                    <div class="mini-text grey--text mt-1">+62 8745 8541 5888</div>
                  </v-col>

                  <v-col md="3">
                    <v-btn small outlined color="grey">
                      <v-icon small>
                        email
                      </v-icon>
                    </v-btn>
                  </v-col>
                  <v-col md="8">
                    <div class="mini-text grey--text mt-1">atrem@gmail.com</div>
                  </v-col>
                </v-row>
              </v-col>
              <v-col md="3">
                <div class="text-contain white--text mt-5">
                  Quick Support
                </div>
                <hr style="border:1px solid #FF8F00;width:60%;">
                <v-row>
                  <v-col md="12" class="grey--text mini-text mt-3">
                    <v-icon small left color="amber darken-3">favorite</v-icon>
                    Online Doct
                  </v-col>
                  <v-col md="12" class="grey--text mini-text">
                    <v-icon small left color="amber darken-3">favorite</v-icon>
                    Disccuss with Friend
                  </v-col>
                  <v-col md="12" class="grey--text mini-text">
                    <v-icon small left color="amber darken-3">favorite</v-icon>
                    Carrer Center
                  </v-col>
                  <v-col md="12" class="grey--text mini-text ">
                    <v-icon small left color="amber darken-3">favorite</v-icon>
                    Start Learning
                  </v-col>
                </v-row>
              </v-col>
              <v-col md="3">
                <div class="text-contain white--text mt-5">
                  Instagram
                </div>
                <hr style="border:1px solid #FF8F00;width:50%;">
                <v-row>
                  <v-col md="4" class="pa-1 ma-0" v-for="(image, i) in images" :key="i">
                    <v-img class="ma-0 pa-0" :src="require('../assets/recentRelase/' + image.name)"></v-img>
                  </v-col>
                </v-row>
              </v-col>
              <v-col md="3">
                <div class="text-contain white--text mt-5">
                  Subscribe
                </div>
                <hr style="border:1px solid #FF8F00;width:45%;">
                <v-row>
                  <v-col md="12" class="mini-text grey--text">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. O
                  </v-col>
                  <v-col md="8">
                    <v-text-field
                      label="Email Address"
                      required
                      dark
                    ></v-text-field>
                  </v-col>
                  <v-col md="4">
                    <v-btn color="warning" small class="mt-5">Send</v-btn>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-container>
  </div>
</template>
<script>
export default {
  name:'footer',
  data(){
    return{
      images:[
        {name:'anna-earl-l2ARBUWlHbU-unsplash.png'},
        {name:'annie-spratt-xKJUnFwfz3s-unsplash.png'},
        {name:'clay-banks-NGupON6JOYE-unsplash.png'},
        {name:'neonbrand-gYf49RB7bvE-unsplash.png'},
        {name:'neonbrand-y_6rqStQBYQ-unsplash.png'},
        {name:'next-academy-JyJwO0K5fWM-unsplash.png'},
      ]
    }
  }
}
</script>
<style scoped>
  .bg-footer{
    background-image: url('../assets/footer/Mask Group 10.png');
    background-size: cover;
  }
  .mini-text{
    font-size: 5px;
  }
</style>