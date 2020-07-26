<template>
  <div>
    <v-container class="mt-5 mb-5">
      <v-row>
        <v-col md="10" class="text-center" offset="1">
          <div class="text-h5 font-weight-bold">Latest <span class="amber--text text--darken-3">News Update</span></div>
          <div class="text-caption">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium esse maxime repudiandae qui suscipit commodi nisi numquam accusamus ipsam, ad expliclorem lorem iandae qui suscipit commodi nisi numquam accusamus ipsam, ad expliclorem lorem </div>
          <v-row>
            <v-col md="4" v-for="(news, i) in newss" :key="i">
              <v-row>
                <v-col md="11" offset-md="1" class="text-caption">
                  <v-img :src="require('../assets/news/' + news.img)">
                    <div class="event-date-cover white--text">
                      <p class="text--caption">{{news.date}} <br> {{news.month}}</p> 
                    </div>
                  </v-img>
                  <v-col md="12" class="text-caption text-center white--text" style="background-color:#FF8F00;">
                    <v-icon small color="white">person</v-icon> {{news.writter}}
                    <v-icon small color="white" right>comment</v-icon> {{news.total}}
                    <v-icon small color="white" right>reply</v-icon> {{news.total2}}
                  </v-col>
                  {{news.desc}}
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name:'news',
  data(){
    return{
      newss:[
        {
          date:'31',
          month:'Aug',
          title:'Design Tips',
          desc:'adipisicing elit. Aut quisquam necessitatibus  eum adipisci',
          img:'wonderlane-w1s5H_3Zn48-unsplash.png',
          total:17,
          total2:32,
          writter:'Mrs. Cecilia'
        },
        {
          date:'10',
          month:'May',
          title:'How to be good Programmer',
          desc:'adipisicing elit. Aut quisquam necessitatibus  eum adipisci',
          img:'priscilla-du-preez-Q7wGvnbuwj0-unsplash.png',
          total:27,
          total2:45,
          writter:'Mr. Edward'
        },
        {
          date:'31',
          month:'Aug',
          title:'How to improve your skill',
          desc:'adipisicing elit. Aut quisquam necessitatibus  eum adipisci',
          img:'product-school-zFBVxClB2I8-unsplash.png',
          total:37,
          total2:86,
          writter:'Mr. David'
        },
      ]
    }
  }
}
</script>
<style scoped>
  .event-date-cover{
      position: absolute;
      background-color:#FF8F00;
      padding:5px 15px 0px;
    }
</style>