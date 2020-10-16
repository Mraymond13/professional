

<template>
   
   <div>
    <v-toolbar
    align-items="left"
     height="300%"
      dark
      prominent
      src="https://images.pexels.com/photos/583847/pexels-photo-583847.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
    >
     

      <v-toolbar-title>Matthew Raymond</v-toolbar-title>

      <v-spacer></v-spacer>

     
        <v-app-bar-nav-icon
       
          dark
          @click.stop="drawer = !drawer"
        >
      
       </v-app-bar-nav-icon>
   
      <v-btn icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>
    </v-toolbar>
   <v-sheet
    height="400"
    class="overflow-hidden"
    style="position: relative;"
  >
 

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://media-exp1.licdn.com/dms/image/C4E35AQF0n_grf5Pu7g/profile-framedphoto-shrink_200_200/0?e=1602093600&v=beta&t=e9LWXLaszF2j6ZHKJUjnYpARHHgLfcUwioSDFZxG_EA"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Matthew Raymond</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>
   <v-container v-for="item in items" :key="item.val" class="background">
       <div class="d-flex flex-no-wrap justify-space-between">
    <v-row :class="item.val">
      <v-col xs2>
      

          <v-card
 
     
       

  
    outlined
  >

  
    <v-list-item three-line>
      <v-list-item-content>
        <div class="overline mb-4">
          OVERLINE
        </div>
        <v-list-item-title class=text-center>
          Headline 5
        </v-list-item-title>
        <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>
  <v-avatar  class="profile"
               
                size="125"
               tile
              >
         <v-img src="https://cf.geekdo-images.com/itemrep/img/090OjiBLiShq_iqolethdTkegrY=/fit-in/246x300/filters:strip_icc()/pic4581181.jpg"> </v-img>
              </v-avatar>
    <v-card-actions>

     
      <v-btn
        outlined
        rounded
        text
      >
        Button
      </v-btn>

    </v-card-actions>

  
  </v-card>

 
</v-col>

 </v-row>

</div>
    
    
    </v-container>
 
  </v-sheet>
 <div id="app">

</div>



    <v-main>
      <HelloWorld/>
    </v-main>
    </div>
</template>

<style >

.v-card > .v-avatar {
  border-radius: 0%;
  justify-content: right;
  justify-items: right;
  align-content: right;
  align-items: right;
}

</style>

<script>
import Vue from 'vue'
import App from './App.vue'

new Vue({
  el: App,
  data() {
    return {
      items: [
       
        {val: 'justify-center'}
      ]
    }
  }
})

  export default {
   data () {
   return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],
      }
   }
  }





       
   
 
</script>
