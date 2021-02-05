<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2 font-italic">{{ title }}</h6>
    <Dialog />

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in freshPasta"
            :key="item.id"
            :url="item.url"
            :title="item.title"
            :type="item.type"
            :img="item.img"
            :text="item.text"
            :reviews="item.reviews"
            :value="item.value"
            :chef="item.chef"
        />
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
import mainComponent from "@/components/mainComponent";
import Dialog from "@/components/UI/Dialog";

export default {
  name: "Vegetarian",
  components: {
    mainComponent,
    Dialog
  },
  data() {
    return {
      title: "Fresh Pasta",
      freshPasta: [
        {
          title: "Pasta",
          id: "p1",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 223,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img:"https://images.unsplash.com/photo-1528658948776-cf610b846f80?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8Y2FyYm9uYXJhfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Pasta ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.unsplash.com/photo-1598866594230-a7c12756260f?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=911&q=80"

        },
        {
          title: "Pasta ",
          id: "p3",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi V.",
          img:"https://images.unsplash.com/photo-1516685018646-549198525c1b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8N3x8cGFzdGF8ZW58MHwwfDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"

        },
        {
          title: "Pasta ",
          id: "p4",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          img:"https://images.unsplash.com/photo-1587394214354-a427608f15cc?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fHBhc3RhfGVufDB8MHwwfA%3D%3D&auto=format&fit=crop&w=500&q=60"

        },
        {
          title: "Pasta ",
          id: "p5",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          favorite: true,
          chef: "Gigi R",
          img:"https://images.unsplash.com/photo-1567608285969-48e4bbe0d399?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTR8fHBhc3RhfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"

        },
        {
          title: "Pasta ",
          id: "p6",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          img:"https://images.unsplash.com/photo-1553842305-95ade71145ff?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mzd8fHBhc3RhfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"

        },
        {
          title: "Pasta ",
          id: "p7",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          img:"https://images.pexels.com/photos/1279330/pexels-photo-1279330.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p8",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.pexels.com/photos/1438672/pexels-photo-1438672.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.pexels.com/photos/1487511/pexels-photo-1487511.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "onion soup",
          id: "p10",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.7,
          reviews: 33,
          favorite: true,
          chef: "Didina B",
          img:"https://images.pexels.com/photos/1256875/pexels-photo-1256875.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p11",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          img:"https://images.pexels.com/photos/1150447/pexels-photo-1150447.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p12",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          img:"https://images.pexels.com/photos/3209101/pexels-photo-3209101.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.pexels.com/photos/2412950/pexels-photo-2412950.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p14",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.pexels.com/photos/688804/pexels-photo-688804.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
        },
        {
          title: "Pasta ",
          id: "p15",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          img:"https://images.pexels.com/photos/3214160/pexels-photo-3214160.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"

        },
        {
          title: "Pasta ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.unsplash.com/photo-1574926053821-79c5e338a933?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"

        },

      ]
    }
  },
}
</script>

<style scoped>

</style>