<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2 font-italic">{{ title }}</h6>
    <Dialog />

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in vegetarians"
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
      title: "Vegetarians",
      vegetarians: [
        {
          title: "Vegetarian  .. ",
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
          title: "Vegetarian  .. ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1490645935967-10de6ba17061?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8dmVnZXRhcmlhbnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"

        },
        {
          title: "Vegetarian  .. ",
          id: "p3",
          type: "vegan",
          text: "See the recipe here",

          value: 2.5,
          reviews: 523,
          img: "https://images.unsplash.com/photo-1510431198580-7727c9fa1e3a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Gigi V.",

        },
        {
          title: "Vegetarian  .. ",
          id: "p4",
          type: "vegan",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          img: "https://images.unsplash.com/photo-1547592166-23ac45744acd?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=751&q=80",
          favorite: true,
          chef: "Marian P",

        },
        {
          title: "Vegetarian  .. ",
          id: "p5",
          type: "vegan",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          img: "https://images.unsplash.com/photo-1578861256505-d3be7cb037d3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Gigi R",

        },
        {
          title: "Vegetarian  .. ",
          id: "p6",
          type: "vegan",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          img: "https://images.unsplash.com/photo-1542986130-d0c46350cf30?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTZ8fHZlZ2V0YXJpYW58ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Angela B",

        },
        {
          title: "Vegetarian  .. ",
          id: "p7",
          type: "vegan",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          img: "https://images.unsplash.com/photo-1578859318509-62790b079366?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=340&q=80",
          favorite: true,
          chef: "Vasilica B"

        },
        {
          title: "Vegetarian  .. ",
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
          title: "Vegetarian  .. ",
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
          type: "raw-vegan",
          text: "See the recipe here",
          value: 2.7,
          reviews: 33,
          img: "https://images.unsplash.com/photo-1549396563-92fab230895a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          favorite: true,
          chef: "Didina B"
        },
        {
          title: "Vegetarian  .. ",
          id: "p11",
          type: "raw-vegan",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          img: "https://images.unsplash.com/photo-1605909388460-74ec8b204127?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          favorite: true,
          chef: "Ionela S"
        },
        {
          title: "Vegetarian  .. ",
          id: "p12",
          type: "raw-vegan",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          img: "https://images.unsplash.com/photo-1560684352-8497838a2229?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=456&q=80",
          favorite: true,
          chef: "Mariana B"

        },
        {
          title: "Vegetarian  .. ",
          id: "p13",
          type: "raw-vegan",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          img: "https://images.unsplash.com/photo-1578020190125-f4f7c18bc9cb?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=375&q=80",
          favorite: true,
          chef: "Ionel B"
        },
        {
          title: "Vegetarian  .. ",
          id: "p14",
          type: "raw-vegan",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          img: "https://images.unsplash.com/photo-1568625365131-079e026a927d?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTF8fHZlZ2V0YXJpYW58ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "Vegetarian  .. ",
          id: "p15",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          img: "https://images.unsplash.com/photo-1563866715647-f42420ed5ccc?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDl8fHZlZ2V0YXJpYW58ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Gigina B"
        },
        {
          title: "Vegetarian  .. ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          img: "https://images.unsplash.com/photo-1518779578993-ec3579fee39f?ixid=MXwxMjA3fDB8MHxzZWFyY2h8ODR8fHZlZ2V0YXJpYW58ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Ionel B"

        },

      ]
    }
  },
}
</script>

<style scoped>
.true{
  color: red;
}

</style>