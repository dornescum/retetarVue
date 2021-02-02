<template>
  <v-container class="grey lighten-5">

    <v-layout class="ma-1">
    <v-btn >
      <v-icon>mdi-folder</v-icon>
      <span class="caption" > by ingredient</span>
    </v-btn>
    <v-btn>test</v-btn>
    </v-layout>


    <v-row>
      <v-col
          v-for="item in pasta"
          :key="item.id"
          cols="12"
          sm="6"
          md="6"
          lg="6"
          outline
      >
      <v-flex>
        <v-card
            class="pa-5"
            outlined
            tile
        >
          <h3>  {{ item.title }} </h3>

          <v-icon :class='`pa-3 ${item.favorite}`' @click="heart = !heart">mdi-heart</v-icon>
          <p>
            Ingrediaents:
          </p>
          <v-flex>
            {{ item.ingredients }}

          </v-flex>
          <p>Description:</p>
          <v-flex>
            {{ item.text }}
          </v-flex>


          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                  color="primary"
                  dark
                  v-bind="attrs"
                  v-on="on"
              >
                Top
              </v-btn>
            </template>
            <span>Top tooltip</span>
          </v-tooltip>


        </v-card>
        <v-img :src="item.img" height="400px" width="500px"></v-img>

        <v-divider></v-divider>
      </v-flex>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Pasta",
  data() {
    return {
      heart: false,
      pasta: [
        {
          title: "pasta 1",
          id: "p1",
          ingredients: "bla, bla",
          text: "description of the recipe",
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true
        },
        {
          title: "pasta 2",
          id: "p2",
          ingredients: "bla, bla, onion",
          text: "description",
          img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",
          favorite: false
        },
        {
          title: "pasta 3",
          id: "p3",
          text: "description",
          img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",

          favorite: false
        },
        {
          title: "pasta 4",
          id: "p4",
          text: "description",
          img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",

          favorite: false
        },

      ]
    }
  },
  methods:{
    // lightHeart(){
    //   if (this.heart){
    //   }
    //   else{
    //
    //   }
    // }
    // byIngredient(item){
    //   this.pasta.sort((a,b)=>{a[item]< b[item] ? -1 : 1})
    // }
  }
}
</script>

<style scoped>
.true{
  color: red;
}
</style>