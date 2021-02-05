<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2">{{ title }}</h6>
    <Dialog />
    <v-col>
      <v-row>
        <mainComponent
            v-for="item in meats"
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
  components: {
    mainComponent,
    Dialog
  },
  name: "Meats",
  data() {
    return {
      title: "Meats",
      meats: [
        {
          title: "Steak .. ",
          id: "p1",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 223,
          img: "https://images.unsplash.com/photo-1565299715199-866c917206bb?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Ionel B",
          url: "/pasta"
        },
        {
          title: "Steak .. ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1594041680534-e8c8cdebd659?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NXx8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p3",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi V.",
          img: "https://images.unsplash.com/photo-1583953623787-ada99d338235?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",

        },
        {
          title: "Steak .. ",
          id: "p4",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          img: "https://images.unsplash.com/photo-1588347818036-558601350947?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NHx8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p5",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          img: "https://images.unsplash.com/photo-1600891964092-4316c288032e?ixid=MXwxMjA3fDB8MHxzZWFyY2h8N3x8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          favorite: true,
          chef: "Gigi R",

        },
        {
          title: "Steak .. ",
          id: "p6",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          img: "https://images.unsplash.com/photo-1546964124-0cce460f38ef?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nnx8c3RlYWt8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p7",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          img: "https://images.unsplash.com/photo-1544025162-d76694265947?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTR8fHN0ZWFrfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p8",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1606419420761-4f2aa891ed19?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTZ8fHN0ZWFrfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1571162242324-f1607b1eceaa?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTh8fHN0ZWFrfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "onion soup",
          id: "p10",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.7,
          reviews: 33,
          favorite: true,
          chef: "Didina B",
          img: "https://images.unsplash.com/photo-1558199141-391d935676f0?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTl8fHN0ZWFrfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p11",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          img: "https://images.unsplash.com/photo-1608877906884-5ffef2ef9612?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzN8fHN0ZWFrfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          title: "Steak .. ",
          id: "p12",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          img: "https://images.pexels.com/photos/769289/pexels-photo-769289.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
        },
        {
          title: "Steak .. ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.pexels.com/photos/675951/pexels-photo-675951.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
        },
        {
          title: "Steak .. ",
          id: "p14",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.pexels.com/photos/3997609/pexels-photo-3997609.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
        },
        {
          title: "Steak .. ",
          id: "p15",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          img: "https://images.pexels.com/photos/299348/pexels-photo-299348.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
        },
        {
          title: "Steak .. ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.pexels.com/photos/341044/pexels-photo-341044.png?auto=compress&cs=tinysrgb&dpr=1&w=500",
        },

      ]
    }
  }
}
</script>

<style scoped>

</style>