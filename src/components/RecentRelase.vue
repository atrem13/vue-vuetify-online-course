<template>
  <div> 
    <v-container class="mt-5 mb-5">
      <v-row>
        <v-col
          md="10"
          offset-md="1"
          class="text-center"
        >
          <div class="text-h5 mb-3 font-weight-bold ">Recent <span class="amber--text text--darken-3 ">Relase</span></div>
          <p class="text-caption mb-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae voluptates nam amet quaerat. Sit, earum quos corporis dolorem similique voluptates aliquam, non rem explicabo labore error dolorum eaque animi dolore?</p>
          <v-row>
            <v-col
              md="12"
              class="mb-5"
              style="border-top:1px solid grey;border-bottom:1px solid grey;"
            >
              <v-btn 
                small 
                text
                v-for="(kategori, i) in kategoris"
                :key="i"
                class="text-caption"
              >
                {{kategori.title}}
              </v-btn>
              
            </v-col>
            <v-col
              md="4"
              v-for="(r_relase, i) in r_relases"
              :key="i"
              style="position:relative;"
              class="img-recent-relase"
            >
              <v-img
                height="200"
                :src="require('../assets/recentRelase/' + r_relase.img)"
              >
              <div class="cover-recent-relase">
                <v-container style="height:100%;">
                  <v-row align="center" style="height:100%;">
                    <v-col
                      md="12"
                      style="background-color:#FF8F00"                    
                    >
                      <div class="text-h5">
                        <v-btn
                          outlined
                          fab
                          color="white"
                          x-small
                          class="mr-3"
                        >
                          <v-icon>favorite</v-icon>
                        </v-btn>
                        <v-btn
                          outlined
                          fab
                          color="white"
                          x-small
                        >
                          <v-icon>visibility</v-icon>
                        </v-btn>
                      </div>
                      <div class="text-h6 white--text">{{r_relase.title}}</div> 
                    </v-col>
                  </v-row>
                </v-container>
              </div>

              </v-img>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name:'recentrelase',
  data(){
    return{
      kategoris: [
        {
          title: 'All'
        },
        {
          title: 'Art & Design'
        },
        {
          title: 'Programming'
        },
        {
          title: 'Auto Mobiles'
        },
        {
          title: 'Robotics'
        },
        {
          title: 'Photography'
        },

      ],
      r_relases: [
        {
          img:'anna-earl-l2ARBUWlHbU-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'annie-spratt-xKJUnFwfz3s-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'clay-banks-NGupON6JOYE-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'neonbrand-gYf49RB7bvE-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'neonbrand-y_6rqStQBYQ-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'next-academy-JyJwO0K5fWM-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'product-school-YrJ99TBRQvI-unsplash.png',
          title:'Web Developer'
        },
        {
          img:'tim-gouw-1K9T5YiZ2WU-unsplash.png',
          title:'Web Developer'
        },
        
      ]
    }
  }
}
</script>
<style scoped>
  .cover-recent-relase{
    height: 100%;
    width: 100%;
    position:absolute;
    background-color: rgba(0, 0, 0, 0.8);
    display: none;
  }
  .img-recent-relase:hover .cover-recent-relase{
    display: block;
  }
</style>