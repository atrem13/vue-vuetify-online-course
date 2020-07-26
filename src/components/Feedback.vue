<template>
  <div>
    <v-container fluid class="mt-5 bg-feedback mb-5">
      <v-container>
        <v-row class="mt-5">
          <v-col md="6" offset-md="4">
            <v-card>
              <v-card-text>
                <div class="text-caption font-weight-bold">Testimonial</div>
                <div class="text-h5 font-weight-bold black--text">Encoraging <span class="amber--text text--darken-3">Feedback</span></div>
                <hr style="border:2px solid #FF8F00; width:23%;margin:10px 0;">
                <div class="text-caption mb-5 font-italic font-weight-thin">"Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo veniam doloribus aliquid perferendis voluptas voluptates molestias delectus quae sed minus laborum fuga labore necessitatibus autem, saepe, laboriosam vitae maxime beatae."</div>
                <v-row>
                  <v-col md="2">
                    <v-img height="50" contain src="../assets/encourage/quote.png"></v-img>
                  </v-col>
                  <v-col md="3">
                    <div class="text-h6">Merta Yoga</div>
                    <div class="text-caption">Idiot Human</div>
                  </v-col>
                </v-row>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-container>
  </div>
</template>
<script>
export default {
  name: 'feedback',
  data(){
    return{

    }
  }
}
</script>
<style scoped>
  .bg-feedback{
    background-image: url('../assets/encourage/Mask Group 9.png');
    background-size: cover;
  }
</style>