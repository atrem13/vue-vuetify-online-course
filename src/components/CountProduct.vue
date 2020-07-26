<template>
  <div>
    <v-container style="background-color:#FF8F00" fluid>
      <v-row>
        <v-col
          md="8"
          offset-md="2"
        >
          <v-row>
            <v-col
              md="3"
              v-for="(product, i) in products"
              :key="i" 
            >
              <v-row>
                <v-col
                  md="4"
                >
                  <v-icon class="mt-3" x-large left>
                    {{product.icon}}
                  </v-icon>
                </v-col>
                <v-col
                  md="8"
                >
                  <div class="white--text text-h5">{{product.title}}</div>
                  <div class="text-h4 font-weight-bold">{{product.total}}+</div>
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
  name:'countproduct',
  data(){
    return{
      products:[
        {
          title:'E-Books',
          icon:'laptop_chromebook',
          total:76
        },
        {
          title:'Audios',
          icon:'volume_up',
          total:211
        },
        {
          title:'Notes',
          icon:'description',
          total:142
        },
        {
          title:'Videos',
          icon:'video_call',
          total:355
        },
        
      ]
    }
  }
}
</script>