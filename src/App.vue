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
  </v-sheet>


    <v-main>
      <HelloWorld/>
    </v-main>
    </div>
</template>

<script>


  export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],
      }
    },
  }
</script>
