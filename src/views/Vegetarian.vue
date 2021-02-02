<template>
<v-container class="my-5">
  <v-layout row wrap>
    <v-flex xs12 sm6 md4 lg3 v-for="item in pasta" :key="item.id">
        <v-card class="text-center ma-3">
          <v-responsive class="pt-4" :src="item.img">
            <v-img :src="item.img" height="300px" width="500px"></v-img>
          </v-responsive>
          <v-card-text>
            <div class="subheading">{{item.title}}</div>
            <div class="grey--text">{{item.text}}</div>
          </v-card-text>
          <v-card-actions class="justify-center">
            <v-btn color="grey" text>add to favorites</v-btn>
          </v-card-actions>
          <v-responsive class="pt-4">
            <v-flex row class="pa-4 justify-end">
              <p  class="pa-2">test</p>
              <v-avatar  size="40" class="grey lighten-4">
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
export default {
name: "Vegetarian",
  data(){
  return{
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
  }
}
</script>

<style scoped>

</style>