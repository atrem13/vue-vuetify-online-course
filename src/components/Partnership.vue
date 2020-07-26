<template>
  <div>
    <v-container class="bg-partnership mt-5 mb-5" fluid>
      <v-container>
        <v-row>
          <v-col
            md="10"
            offset-md="1"
          >
            <div class="mt-5 text-h5 font-weight-bold text-center">
              Our <span class="white--text">Partnership</span>
            </div>
            <div class="text-content text-center mt-3">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam natus reiciendis sint debitis distinctio! Error beatae magni, minus recusandae numquam odit pariatur. Voluptatibus omnis expedita facere ipsam laboriosam illo esse?</div>
            <v-sheet
              class="mx-auto"
              elevation="0"
              color="transparent"
            >
              <v-slide-group
                v-model="model"
                class="pa-4"
                show-arrows
              >
                <v-slide-item
                  v-for="(partnership, i) in partnerships"
                  :key="i"
                >
                  <v-card
                    class="ma-4"
                    elevation="0"
                    width="130"
                    color="transparent"
                  >
                    <v-img
                      :src="require('../assets/brand/' + partnership.img)"
                      class="brand-image"
                    >

                    </v-img>
                    <v-row
                      class="fill-height"
                      align="center"
                      justify="center"
                    >
                      <v-scale-transition>
                        <v-icon
                          v-if="active"
                          color="white"
                          size="48"
                          v-text="'mdi-close-circle-outline'"
                        ></v-icon>
                      </v-scale-transition>
                    </v-row>
                  </v-card>
                </v-slide-item>
              </v-slide-group>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-container>
  </div>
</template>
<script>
export default {
  name:'partnership',
  data(){
    return{
      partnerships:[
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        {
          img:'logo-png-images-download-122638-png-resources-with-transparent-brand-png-360_360.png'
        },
        { 
          img:'unnamed.png'
        },
        
      ]
    }
  }
}
</script>
<style scoped>
  .bg-partnership{
    background-image: url('../assets/brand/Group 7.png');
    background-size: cover;
  }
  .brand-image{
    filter:invert(100%);
  }
</style>
