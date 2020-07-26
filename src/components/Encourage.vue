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
              md="5"
            >
              <v-img
                src="../assets/encourage/purepng.com-pewdiepie-holding-bookpeoplepersonsyoutubersyoutubepewdiepie-251520169613mdpjl.png"
              >

              </v-img>
            </v-col>
            <v-col
              md="7"
              class="text-center"
            >
              <div class="text-h5 font-weight-bold" style="margin-top:80px">Why Choose <span class="amber--text text--darken-3">Atrem Educate</span></div>
              <div class="text-caption">Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni id accusantium vitae dolorem illo consequatur officia fugiat voluptate quibusd</div>
              <v-row class="mt-5">
                <v-col
                  md="6"
                  class="mb-5"
                  v-for="(benefit, i) in benefits"
                  :key="i"
                >
                  <v-icon color="amber darken-3">
                    {{benefit.icon}}
                  </v-icon>
                  <div class="text-h6 mt-5">{{benefit.title}}</div>
                  <div class="text-body-2 font-weight-thin grey--text">{{benefit.content}}</div>
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
  name:'encourage',
  data(){
    return{
      benefits:[
        {
          icon: 'important_devices',
          title: 'Learn with Device',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni id accusantium vitae d'
        },
        {
          icon: 'send',
          title: 'Fastest Support',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni id accusantium vitae d'
        },
        {
          icon: 'how_to_reg',
          title: 'Certified Teachers',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni id accusantium vitae d'
        },
        {
          icon: 'timer',
          title: 'Flexible Time Frame',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni id accusantium vitae d'
        },
      ]
    }
  }
}
</script>