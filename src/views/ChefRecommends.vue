<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2 font-italic">{{ title }}</h6>
    <Dialog />

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in recomandations"
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
      title: "Top dishes",
      recomandations: [
        {
          title: "Foie Gras ...",
          id: "p1",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 223,
          img: "https://images.unsplash.com/photo-1594756202469-9ff9799b2e4e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=335&q=80",
          favorite: true,
          chef: "Ionel B",
          url: "/pasta"
        },
        {
          title: "Soup .. ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          img: "https://images.unsplash.com/photo-1476718406336-bb5a9690ee2a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "Soup .. ",
          id: "p3",
          type: "vegetarian",
          text: "See the recipe here",

          value: 2.5,
          reviews: 523,
          img: "https://images.unsplash.com/photo-1510431198580-7727c9fa1e3a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Gigi V.",

        },
        {
          title: "Soup .. ",
          id: "p4",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          img: "https://images.unsplash.com/photo-1547592166-23ac45744acd?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=751&q=80",
          favorite: true,
          chef: "Marian P",

        },
        {
          title: "Soup .. ",
          id: "p5",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          img: "https://images.unsplash.com/photo-1578861256505-d3be7cb037d3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Gigi R",

        },
        {
          title: "Soup .. ",
          id: "p6",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          img: "https://images.unsplash.com/photo-1534939561126-855b8675edd7?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Angela B",

        },
        {
          title: "Soup .. ",
          id: "p7",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          img: "https://images.unsplash.com/photo-1578859318509-62790b079366?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=340&q=80",
          favorite: true,
          chef: "Vasilica B"

        },
        {
          title: "Soup .. ",
          id: "p8",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          img: "https://images.unsplash.com/photo-1603105037880-880cd4edfb0d?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "Soup .. ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          img: "https://images.unsplash.com/photo-1603208785984-cdf985beca7a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=343&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "onion soup",
          id: "p10",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.7,
          reviews: 33,
          img: "https://images.unsplash.com/photo-1549396563-92fab230895a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Didina B"
        },
        {
          title: "Soup .. ",
          id: "p11",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          img: "https://images.unsplash.com/photo-1605909388460-74ec8b204127?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          favorite: true,
          chef: "Ionela S"
        },
        {
          title: "Soup .. ",
          id: "p12",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          img: "https://images.unsplash.com/photo-1560684352-8497838a2229?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=456&q=80",
          favorite: true,
          chef: "Mariana B"

        },
        {
          title: "Soup .. ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          img: "https://images.unsplash.com/photo-1578020190125-f4f7c18bc9cb?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=375&q=80",
          favorite: true,
          chef: "Ionel B"
        },
        {
          title: "Soup .. ",
          id: "p14",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          img: "https://images.unsplash.com/photo-1598636011724-66aaff2f8bb7?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=752&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "Soup .. ",
          id: "p15",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          img: "https://images.unsplash.com/photo-1608930532174-18ff53f01438?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=401&q=80",
          favorite: true,
          chef: "Gigina B"
        },
        {
          title: "Soup .. ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          img: "https://images.unsplash.com/photo-1611745451987-bd5df5565d9e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=708&q=80",
          favorite: true,
          chef: "Ionel B"

        },

      ]
    }
  },
}
</script>

<style scoped>

</style>