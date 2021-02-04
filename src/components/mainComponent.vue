<template>
<!--  <v-layout row wrap>-->
    <v-flex xs12 sm6 md4 lg3>
      <v-card class=" ma-3">
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

            {{text}}
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
          <v-btn color="grey" text>add to favorites
            <v-icon>mdi-heart</v-icon>
          </v-btn>
        </v-card-actions>
        <v-responsive class="pt-4">
          <v-flex row class="pa-4 justify-end">
            <p class="pa-2"><span class="grey--text font-weight-black">Recipe by :</span>
              <span class="grey--text font-italic pl-2"></span>{{chef}}</p>
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
      // desert: [
      //   {
      //     title: "Fetucine carbonara",
      //     id: "p1",
      //     type:"non-vegetarian",
      //     text:
      //         "Fettuccine Alfredo  is an Italian pasta dish of fresh fettuccine tossed" +
      //         " with butter and Parmesan cheese",
      //     value:4.5,
      //     reviews: 223,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B",
      //     url: "/pasta"
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p2",
      //     type:"non-vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.3,
      //     reviews: 2123,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p3",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:2.5,
      //     reviews: 523,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Croistorasul cel viteaz",
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p4",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.5,
      //     reviews: 723,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Marian P",
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p5",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:3.5,
      //     reviews: 623,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Gigi R",
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p6",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.8,
      //     reviews: 3,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Angela B",
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p7",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.9,
      //     reviews: 43,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Vasilica B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p8",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:2.5,
      //     reviews: 89,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p9",
      //     type:"non-vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:1.5,
      //     reviews: 103,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p10",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:2.7,
      //     reviews: 33,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Didina B"
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p11",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:3.5,
      //     reviews: 13,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionela S"
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p12",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:3.8,
      //     reviews: 24,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Mariana B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p13",
      //     type:"non-vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:3.9,
      //     reviews: 2234,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p14",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:2.8,
      //     reviews: 2235,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p15",
      //     type:"vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.2,
      //     reviews: 213,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Gigina B"
      //   },
      //   {
      //     title: "pasta 1",
      //     id: "p16",
      //     type:"non-vegetarian",
      //     text:
      //         "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
      //     value:4.3,
      //     reviews: 293,
      //     img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
      //     favorite: true,
      //     chef: "Ionel B"
      //
      //   },
      //
      // ]
    }
  }
}
</script>

<style scoped>

</style>