<template>
  <div>
    <v-container class="mt-5 mb-5">
      <v-row>
        <v-col
          md="10"
          offset-md="1"
        >
          <v-row>
            <v-col
              md="12 mb-5"
            >
              <div class="text-h5 font-weight-bold">Upcoming <span class="amber--text text--daken-3">Event</span></div>
              <div class="text-content" style="width:55%">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut quisquam necessitatibus accusantium, repudiandae dignissimos eum adipisci, </div>
            </v-col>
          </v-row>
          <v-row
            v-for="(event, i) in events"
            :key="i"
            class="mb-5">
            <v-col
              md="4"
              style="position:relative;"
            >
              <v-img
                :src="require('../assets/event/' + event.img)"
              >
                <div class="event-date-cover text-center white--text">
                  <div class="text-h6 ma-0 pa-0">{{event.date}}</div>
                  <div class="text-caption ma-0 pa-0">{{event.month}}</div>
                </div>
              </v-img>
            </v-col>
            <v-col
              md="5"
            > 
              <div class="text-h6 font-weight-bold">{{event.title}}</div>
              <div class="text-caption grey--text">{{event.desc}}</div>
            </v-col>
            <v-col
              md="3"
              style="border-left:1px solid grey">
              <v-row>
                <v-col md="2">
                  <v-btn
                    outlined
                    x-small
                    color="amber darken-3"
                  >
                    <v-icon small>
                      location_on
                    </v-icon>
                  </v-btn>
                </v-col>
                <v-col md="10">
                  <div class="mt-1 ml-2 text-caption">{{event.loct}}</div>
                </v-col>
              </v-row>

              <v-row>
                <v-col md="2">
                  <v-btn
                    outlined
                    x-small
                    color="amber darken-3"
                  >
                    <v-icon small>
                      schedule
                    </v-icon>
                  </v-btn>
                </v-col>
                <v-col md="10">
                  <div class="mt-1 ml-2 text-caption">{{event.time}}</div>
                </v-col>
              </v-row>

              <v-row>
                <v-col md="2">
                  <v-btn
                    outlined
                    x-small
                    color="amber darken-3"
                  >
                    <v-icon small>
                      perm_identity
                    </v-icon>
                  </v-btn>
                </v-col>
                <v-col md="10">
                  <div class="mt-1 ml-2 text-caption">{{event.speaker}}</div>
                </v-col>
              </v-row>
              
            </v-col>
          </v-row>
          <v-row>
            <v-col md="12">
              <v-btn outlined color="grey">View More</v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name: 'upcomingevent',
  data(){
    return{
      events: [
        {
          date:'10',
          month:'Nov',
          title:'Reactjs Bootcamp',
          desc:'adipisicing elit. Aut quisquam necessitatibus accusantium, repudiandae dignissimos eum adipisci',
          img:'hello-i-m-nik-73_kRzs9sqo-unsplash.png',
          loct:'Kembali Hub',
          time:'15:00-19:00',
          speaker:'Mr. Johnatan Erlic'
        },
        {
          date:'31',
          month:'Dec',
          title:'End Year Party',
          desc:'adipisicing elit. Aut quisquam necessitatibus accusantium, repudiandae dignissimos eum adipisci',
          img:'alasdair-elmes-ULHxWq8reao-unsplash.png',
          loct:'Denpasar Industry Center',
          time:'19:00-End',
          speaker:'Mrs. Cecilia'
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
    padding:5px 15px;
  }
</style>