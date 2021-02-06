<template>
<!--  <v-layout row wrap>-->
    <v-flex xs12 sm6 md4 lg3>
<!--      fixme clasa x si y-->
      <v-card class="ma-1">
        <a :href="url">
          <v-responsive class="pt-4">
            <v-img :src="img" height="300px" width="500px">
            </v-img>
          </v-responsive>
        </a>

        <v-card-text>
          <div class="subheading text-center text-capitalize">{{ title }}</div>

          <div class="text-capitalize ma-2 pa-2 font-weight-black">
            {{ type }}
          </div>
          <div class="grey--text pa-3">

            {{text }}
            <a href="#" class="black--text "> ...</a>
          </div>
          <!--            rating-->
          <v-row
              align="center"
              class="mx-2 my-5"
          >
            <v-rating
                :value="value"
                color="amber"
                dense
                half-increments
                readonly
                size="14"
            ></v-rating>
            <div class="grey--text ml-4">
              {{value}} / {{reviews}}
            </div>
          </v-row>
        </v-card-text>
        <!--          chef-->
        <v-card-actions class="justify-center">
          <v-btn color="grey" text> add to favorites
            <v-icon>mdi-heart</v-icon>
          </v-btn>
        </v-card-actions>
        <v-responsive class="pt-4">
          <v-flex row class="pa-4 justify-end">
            <p class="pa-2"><span class="grey--text font-weight-black">Recipe by :</span>
              <span class="grey--text font-italic pl-2 font-14">{{chef}}</span></p>
            <v-avatar size="40" class="grey lighten-4">
              <img :src="img" alt="">
            </v-avatar>

          </v-flex>

        </v-responsive>
      </v-card>
    </v-flex>
<!--  </v-layout>-->
</template>

<script>
export default {
  name: "desert",
  props: ["title", "text", "id", "description", "img", "reviews", "value", "favorite", "chef", "url", "type"],
  data(){
    return{
    }
  },
  computed:{
    filterRecipes: function (){
      return this.titleR.filter((item)=>{
        return item
      })
    }
  }
}
</script>

<style>
.font-14{
  font-size: 14px;
}
.v-btn > .v-btn__content .v-icon:hover{
  color: red !important;
}
</style>