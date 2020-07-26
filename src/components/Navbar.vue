<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      color="amber darken-3"
      dark
    >
      <v-list dense>
        <v-list-item 
          link 
          v-for="link in links" 
          :key="link.text"
        >
          <v-list-item-action>
            <v-icon>{{link.icon}}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>
              {{link.text}}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>
    <v-app-bar
      app
      color="white"
      flat
      
    >
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
      >
        <v-avatar class="ml-5">
          <v-img
            src="../assets/navbarIcon/e-learning.png"
            height="45"
            contain
          ></v-img>
        </v-avatar>
      </v-app-bar-nav-icon>
      <v-toolbar-title>
        Atrem Educate
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-row>
        <v-col
          md="12"
          lg="12"
          class="hidden-sm-and-down text-right"
        >
          <v-btn 
            small 
            text 
            v-for="link in links" 
            :key="link.text"
            color="amber darken-3"
          >
            <v-icon 
              dark 
              left
            >
              {{link.icon}}
            </v-icon>
            {{link.text}}
          </v-btn>
        </v-col>
      </v-row>
      
    </v-app-bar>
  </div>
</template>
<script>
export default {
  name:"Navbar",
  data(){
    return{
      drawer:false,
      links: [
        {
          text:'Home',
          route:'/',
          icon:'home'
        },
        {
          text:'Course',
          route:'/course',
          icon:'school'
        },
        {
          text:'Benefit',
          route:'/benefit',
          icon:'stars'
        },
        {
          text:'Event',
          route:'/event',
          icon:'date_range'
        },
        {
          text:'News',
          route:'/news',
          icon:'chrome_reader_mode'
        },
        {
          text:'Contact',
          route:'/contact',
          icon:'contact_mail'
        },
      ]
    }
  }
}
</script>