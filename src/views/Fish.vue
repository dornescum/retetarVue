<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2 font-italic">{{ title }}</h6>
    <Dialog/>

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in fish"
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
      title: "Fish",
      fish: [
        {
          title: "Some Fish",
          id: "p1",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 223,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img: "https://images.unsplash.com/photo-1556814901-18c866c057da?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8ZmlzaCUyMGdyaWxsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1593604185466-41d3c2e0f234?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTV8fGZpc2glMjBncmlsbHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p3",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi V.",
          img: "https://images.unsplash.com/photo-1579871494447-9811cf80d66c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8c3VzaGl8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p4",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          img: "https://images.unsplash.com/photo-1534482421-64566f976cfa?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjd8fHN1c2hpfGVufDB8fDB8&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p5",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          favorite: true,
          chef: "Gigi R",
          img: "https://images.unsplash.com/photo-1588791174744-7e9bf4378277?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjd8fGxvYnN0ZXJzJTIwZm9vZHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p6",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          img: "https://images.unsplash.com/photo-1586735464691-8cc258723665?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjl8fGxvYnN0ZXJzJTIwZm9vZHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p7",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          img: "https://images.unsplash.com/photo-1572438631563-a3429408a845?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzV8fGxvYnN0ZXJzJTIwZm9vZHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p8",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1582759777896-0aaa738a5c38?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDB8fGxvYnN0ZXJzJTIwZm9vZHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1560113723-5a9fc711588a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjN8fGxvYnN0ZXJzJTIwZm9vZHxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
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
          img: "https://images.unsplash.com/photo-1605760652327-d25d8305009c?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=967&q=80"
        },
        {
          title: "Some Fish ",
          id: "p11",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          img: "https://images.unsplash.com/photo-1609613107023-41902b70e29f?ixid=MXwxMjA3fDB8MHxzZWFyY2h8N3x8b3lzdGVyc3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p12",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          img: "https://images.unsplash.com/photo-1564675533183-b1a836ec6537?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NzB8fHNocmltcHN8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1539586345401-51d5bfba7ac0?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTF8fHNocmltcHN8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p14",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1605493624448-8efd97c98c91?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mzd8fHNocmltcHN8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p15",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          img: "https://images.unsplash.com/photo-1600265721436-734abbfe2137?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8ZmlzaCUyMHN0ZXd8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Some Fish ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          img: "https://images.unsplash.com/photo-1579421880579-44584c3b1659?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjh8fHN1c2hpfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },

      ]
    }
  },
}
</script>

<style scoped>

</style>