<template>
  <v-container class="my-5">
    <h3 class="text-capitalize text-center pa-2 mb-2">desert</h3>
    <Dialog />
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 lg3 v-for="item in deserts" :key="item.id">
        <v-card class=" ma-3">
          <a v-bind:href="item.url">
            <v-responsive class="pt-4" :src="item.img">
              <v-img :src="item.img" height="300px" width="500px">
              </v-img>
            </v-responsive>
          </a>
          <v-card-text>
            <div class="subheading text-center text-capitalize">{{ item.title }}</div>

            <div class="text-capitalize ma-2 pa-2 font-weight-black">
              {{ item.type }}
            </div>
            <div class="grey--text pa-3">

              {{ item.text }}
              <a href="#" class="black--text "> ...</a>
            </div>
            <!--            rating-->
            <v-row
                align="center"
                class="mx-2 my-5"
            >
              <v-rating
                  :value="item.value"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
              ></v-rating>
              <div class="grey--text ml-4">
                {{ item.value }} /
                {{ item.reviews }}
              </div>
            </v-row>
          </v-card-text>
          <!--          chef-->
          <v-card-actions class="justify-center">
            <v-btn color="grey" text>add to favorites
              <v-icon :class='`pa-3 ${item.favorite}`'>mdi-heart</v-icon>
            </v-btn>
          </v-card-actions>
          <v-responsive class="pt-4">
            <v-flex row class="pa-4 justify-end">
              <p class="pa-2"><span class="grey--text font-weight-black">Recipe by :</span>
                <span class="grey--text font-italic pl-2">{{ item.chef }}</span></p>
              <v-avatar size="40" class="grey lighten-4">
                <img :src="item.img" alt="">
              </v-avatar>

            </v-flex>

          </v-responsive>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Dialog from "@/components/UI/Dialog";
export default {
  name: "Vegetarian",
  components:{
    Dialog
  },
  data() {
    return {
      deserts: [
        {
          title: "Desert 1",
          id: "p1",
          type: "non-vegetarian",
          text:
              "See the recipe here ",
          value: 4.5,
          reviews: 223,
          img: "https://images.unsplash.com/photo-1560269507-9495cdfcadca?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NXx8ZGVzc2VydCUyMHRhYmxlfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Ionel B",
          url: "/pasta"
        },
        {
          title: "Desert 2",
          id: "p2",
          type: "non-vegetarian",
          text:
              "See the recipe here ",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1495147466023-ac5c588e2e94?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NHx8ZGVzc2VydHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 3",
          id: "p3",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi P",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1576618148400-f54bed99fcfd?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fGRlc3NlcnR8ZW58MHx8MHw%3D&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 4",
          id: "p4",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1574085733277-851d9d856a3a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTF8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 5",
          id: "p5",
          type: "vegetarian",
          text: "See the recipe here ",
          value: 3.5,
          reviews: 623,
          favorite: true,
          chef: "Gigi R",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1603339342930-df74f51feb7a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nzl8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 6",
          id: "p6",
          type: "vegetarian",
          text:
              "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1488477181946-6428a0291777?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTV8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 7",
          id: "p7",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1506095619733-3c3ea98fb968?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTZ8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 8",
          id: "p8",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img:"https://images.unsplash.com/photo-1560008581-09826d1de69e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=682&q=80",
        },
        {
          title: "Desert 9",
          id: "p9",
          type: "non-vegetarian",
          text:
              "See the recipe here ",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1547049082-1a12c3bf2366?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTl8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 10",
          id: "p10",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 2.7,
          reviews: 33,
          favorite: true,
          chef: "Didina B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1599785209728-60659c85926d?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzZ8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 11",
          id: "p11",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1600002415506-dd06090d3480?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDZ8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 12",
          id: "p12",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1497729019230-f30736e9864f?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NXx8cGF2bG92YXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 13",
          id: "p13",
          type: "non-vegetarian",
          text:
              "See the recipe here ",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1555526148-0fa555bb2e78?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTl8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 14",
          id: "p14",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1599333521738-7c21be2d7283?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NjF8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 15",
          id: "p15",
          type: "vegetarian",
          text:
              "See the recipe here ",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1573553744177-73dc2d3c8c31?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NjV8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Desert 16",
          id: "p16",
          type: "non-vegetarian",
          text:
              "See the recipe here ",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1584818676680-44804433340c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NzF8fGRlc3NlcnR8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },

      ]
    }
  }
}
</script>

<style scoped>
.true {
  color: red;
}
</style>