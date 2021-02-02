<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2">{{title}}</h6>

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in soups"
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

export default {
  components: {
    mainComponent
  },

  name: "Soups",
  data() {
    return {
      title: "Soups",
      soups: [
        {
          title: "Ciorba de vacuta ",
          id: "p1",
          type: "non-vegetarian",
          text:
              "Fettuccine Alfredo  is an Italian pasta dish of fresh fettuccine tossed" +
              " with butter and Parmesan cheese",
          value: 4.5,
          reviews: 223,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B",
          url: "/pasta"
        },
        {
          title: "pasta 1",
          id: "p2",
          type: "non-vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.3,
          reviews: 2123,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "pasta 1",
          id: "p3",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 2.5,
          reviews: 523,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Croistorasul cel viteaz",

        },
        {
          title: "pasta 1",
          id: "p4",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.5,
          reviews: 723,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Marian P",

        },
        {
          title: "pasta 1",
          id: "p5",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 3.5,
          reviews: 623,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Gigi R",

        },
        {
          title: "pasta 1",
          id: "p6",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.8,
          reviews: 3,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Angela B",

        },
        {
          title: "pasta 1",
          id: "p7",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.9,
          reviews: 43,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Vasilica B"

        },
        {
          title: "pasta 1",
          id: "p8",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 2.5,
          reviews: 89,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "pasta 1",
          id: "p9",
          type: "non-vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 1.5,
          reviews: 103,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "pasta 1",
          id: "p10",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 2.7,
          reviews: 33,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Didina B"
        },
        {
          title: "pasta 1",
          id: "p11",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 3.5,
          reviews: 13,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionela S"
        },
        {
          title: "pasta 1",
          id: "p12",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 3.8,
          reviews: 24,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Mariana B"

        },
        {
          title: "pasta 1",
          id: "p13",
          type: "non-vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 3.9,
          reviews: 2234,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"
        },
        {
          title: "pasta 1",
          id: "p14",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 2.8,
          reviews: 2235,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"

        },
        {
          title: "pasta 1",
          id: "p15",
          type: "vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.2,
          reviews: 213,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Gigina B"
        },
        {
          title: "pasta 1",
          id: "p16",
          type: "non-vegetarian",
          text:
              "description of the recipe  probnabdsa dfsadk ad adf sa asdfa asd adadka",
          value: 4.3,
          reviews: 293,
          img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          favorite: true,
          chef: "Ionel B"

        },

      ]
    }
  }
}
</script>

<style scoped>
.test {
  display: flex;
  flex-wrap: wrap;
}
</style>