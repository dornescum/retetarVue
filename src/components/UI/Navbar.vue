<template>
  <nav>
    <v-app-bar app>
      <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
      <a href="/">
        <v-toolbar-title class="text-capitalize grey--text">
          <span class="font-weight-light d-none d-sm-flex" id="title"> Recipes</span>
        </v-toolbar-title>
      </a>


      <a href="/">
        <v-img
            src="@/assets/logo.svg"
            height="50px" max-width="50px" class="ma-1"></v-img>
      </a>

      <v-spacer></v-spacer>
<!--      <Dialog/>-->
      <Search />
      <a href="/login">
        <v-btn text color="grey" class="d-none d-sm-flex">
          <span>Sign out</span>
          <v-icon right>mdi-export</v-icon>
        </v-btn>
      </a>

    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app class="blue-grey lighten-5">
      <v-row class="mt-5 text-center">
        <v-col>
          <v-avatar size="40">
            <a href="/login">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg">
            </a>
          </v-avatar>
          <p class="grey--text subtitle-1 mt-1">`${user}`</p>
        </v-col>
      </v-row>


      <v-list>
        <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-item-avatar>
            <v-icon color="light-blue accent-3">{{ link.icon }}}</v-icon>
          </v-list-item-avatar>
          <v-list-item-subtitle class="font-weight-black text-capitalize">{{ link.text }}</v-list-item-subtitle>
        </v-list-item>
      </v-list>


      <v-btn text color="grey" id="btnOut">
        <span class="ma-auto">Sign out</span>
        <v-icon right>mdi-export</v-icon>
      </v-btn>

      <v-card
          max-width="400"
          class="mx-auto"
      >
        <v-img
            src="https://images-na.ssl-images-amazon.com/images/I/61VU+Dc4XzL._SX258_BO1,204,203,200_.jpg"
            height="300px"
            dark
        >
          <v-row class="fill-height">
            <v-card-title>
              <!--            <v-btn-->
              <!--                dark-->
              <!--                icon-->
              <!--            >-->
              <!--              <v-icon>mdi-chevron-left</v-icon>-->
              <!--            </v-btn>-->

              <v-spacer></v-spacer>

              <!--            <v-btn-->
              <!--                dark-->
              <!--                icon-->
              <!--                class="mr-4"-->
              <!--            >-->
              <!--              <v-icon>mdi-pencil</v-icon>-->
              <!--            </v-btn>-->

              <!--            <v-btn-->
              <!--                dark-->
              <!--                icon-->
              <!--            >-->
              <!--              <v-icon>mdi-dots-vertical</v-icon>-->
              <!--            </v-btn>-->
            </v-card-title>

            <v-spacer></v-spacer>

            <v-card-title class="white--text pl-12 pt-12">
              <div class="display-1 pl-12 pt-12">
                Books
              </div>
            </v-card-title>
          </v-row>
        </v-img>

        <v-list two-line>
          <v-list-item>
            <v-list-item-icon>
              <v-icon color="light-blue accent-3">
                mdi-phone
              </v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>(650) 555-1234</v-list-item-title>
              <v-list-item-subtitle>Mobile</v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-icon>
              <v-icon>mdi-message-text</v-icon>
            </v-list-item-icon>
          </v-list-item>

          <v-list-item>
            <v-list-item-action></v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>(323) 555-6789</v-list-item-title>
              <v-list-item-subtitle>Work</v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-icon>
              <v-icon>mdi-message-text</v-icon>
            </v-list-item-icon>
          </v-list-item>

          <v-divider inset></v-divider>

          <v-list-item>
            <v-list-item-icon>
              <v-icon color="light-blue accent-3">
                mdi-email
              </v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>aliconnors@example.com</v-list-item-title>
              <v-list-item-subtitle>Personal</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-action></v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>ali_connors@example.com</v-list-item-title>
              <v-list-item-subtitle>Work</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-divider inset></v-divider>

          <v-list-item>
            <v-list-item-icon>
              <v-icon color="light-blue accent-3">
                mdi-map-marker
              </v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>1400 Main Street</v-list-item-title>
              <v-list-item-subtitle>Orlando, FL 79938</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-card>


    </v-navigation-drawer>


  </nav>
</template>

<script>
// import Dialog from "@/components/UI/Dialog";
import Search from "@/components/Search";
export default {
  name: "Navbar",
  components: {
    // Dialog
    Search
  },
  data() {
    return {
      drawer: false,
      innerWidth: 600,
      links: [
        {icon: 'mdi-home ', text: 'Recipes', route: '/'},
        {icon: 'mdi-home ', text: 'chef recommends', route: '/chef'},
        {icon: 'mdi-account ', text: 'starters', route: '/starters'},
        {icon: 'mdi-account ', text: 'soups', route: '/soups'},
        {icon: 'mdi-account ', text: 'fresh pasta', route: '/pasta'},
        {icon: 'mdi-star ', text: 'fish', route: '/fish'},
        {icon: 'mdi-home ', text: 'meat', route: '/meat'},
        {icon: 'mdi-account ', text: 'vegetarian', route: '/vegetarian'},
        {icon: 'mdi-account ', text: 'desert', route: '/desert'},
      ],
    }
  },

}
</script>

<style scoped>
/*#title {*/
/*  font-size: 24px;*/
/*  padding: 2px 10px;*/
/*}*/
  #btnOut {
    display: block;
    margin: 5px auto;
  }
/*@media (max-width: 768px) {*/
/*  #title {*/
/*    display: none;*/
/*  }*/

/*  #btnOut {*/
/*    display: none;*/
/*  }*/
/*}*/
</style>