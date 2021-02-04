<template>
  <!--    <Slider/>-->
  <!--   <v-btn class="hidden-md-only">click</v-btn>-->
  <v-container>
    <h1 class="text-capitalize text-center my-3">{{title}}</h1>
    <v-row>
      <v-col xs12 sm6 md4 lg3>
        <v-flex row>

          <v-card v-for="item in categories" :key="item.id"
              class="mx-auto my-2"
              max-width="380"
          >
            <v-img
                class="white--text align-end"
                height="200px"
                :src="item.src"
            >
              <v-card-title>{{item.categoryName}}</v-card-title>
            </v-img>

            <v-card-subtitle class="pb-0">
              {{item.subTitle}}
            </v-card-subtitle>

            <v-card-text class="text--primary">
              <div>{{item.text}}</div>
            </v-card-text>

            <v-card-actions>
              <v-btn
                  color="orange"
                  text
              >
                Share
              </v-btn>
              <a :href="item.route">

                <v-btn
                    color="orange"
                    text
                >
                  Explore
                </v-btn>
              </a>

            </v-card-actions>
          </v-card>



        </v-flex>


      </v-col>
    </v-row>
  </v-container>


</template>

<script>
// @ is an alias to /src
// import Slider from "@/components/Slider";
export default {
  name: 'Home',
  data(){
    return{
      title: "recipes",
      categories : [
        {categoryName: "chef recommends", text: "some shit", subTitle: "more shit" ,id: "g1", route : "/",
          src:"https://images.unsplash.com/photo-1579712267685-42da80f60aa4?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"},
        {categoryName: "starters", text: "some shit", subTitle: "more shit" ,id: "g2", route : "/starters",
          src:"https://images.unsplash.com/photo-1580376259349-5f4b7db4c39f?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"},
        {categoryName: "soup", text: "some shit", subTitle: "more shit" ,id: "g3", route : "/soups",
          src:"https://images.unsplash.com/photo-1547592166-23ac45744acd?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nnx8c291cHxlbnwwfHwwfA%3D%3D&auto=format&fit=crop&w=500&q=60"},
        {categoryName: "fresh pasta", text: "some shit", subTitle: "more shit" ,id: "g4", route : "/pasta",
          src:"https://images.unsplash.com/photo-1520806004693-db86ec088635?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1056&q=80"},
        {categoryName: "fish", text: "some shit", subTitle: "more shit" ,id: "g5", route : "/fish",
          src:"https://images.unsplash.com/photo-1556814901-18c866c057da?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8ZmlzaCUyMGdyaWxsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"},
        {categoryName: "meat", text: "some shit", subTitle: "more shit" ,id: "g6", route : "/meat",
          src:"https://images.pexels.com/photos/769289/pexels-photo-769289.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"},
        {categoryName: "vegetarian", text: "some shit", subTitle: "more shit" ,id: "g7", route : "/vegetarian",
          src:"https://images.unsplash.com/photo-1530912585210-7916cd026e59?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8dmVnZXRhcmlhbiUyMGZvb2R8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"},
        {categoryName: "desserts", text: "some shit", subTitle: "more shit" ,id: "g8", route : "/desert",
          src:"https://images.unsplash.com/photo-1600002415506-dd06090d3480?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDZ8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"},
      ]
    }
  },
  components: {
    // Slider
  }
}
</script>
<style>
a {
  text-decoration: none;
}
.row {
  margin: 0;
}
</style>
