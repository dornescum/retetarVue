<template>
  <v-container>
    <h6 class="grey--text text-center text-capitalize ma-2 font-italic">{{ title }}</h6>
    <Dialog />

    <v-col>
      <v-row>
        <mainComponent
            v-for="item in starters"
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
      title: "Starters",
      starters: [
        {
          title: "Carpacio .. ",
          id: "p1",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 223,
          favorite: true,
          chef: "Ionel B",
          url: "/pasta",
          img:"https://images.unsplash.com/photo-1580302498882-b5aa77f09b75?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTF8fHN0YXJ0ZXJzfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Starter .. ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.unsplash.com/photo-1580638149300-65f0b9e8fbff?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"
        },
        {
          title: "Tartar .. ",
          id: "p3",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi V.",
          img:"http://storage0.dms.mpinteractiv.ro/media/2/2621/33527/16244250/3/11141598-l.jpg"
        },
        {
          title: "Starter .. ",
          id: "p4",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          img:"https://images.unsplash.com/photo-1576670392216-eb265264c057?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjR8fHN0YXJ0ZXJzfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Starter .. ",
          id: "p5",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          favorite: true,
          chef: "Gigi R",
          img:"https://images.unsplash.com/photo-1579631542761-d7c4e913f8d4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjZ8fHN0YXJ0ZXJzfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Starter .. ",
          id: "p6",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          img:"https://images.unsplash.com/photo-1576831438132-7b74c94006b2?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjV8fHN0YXJ0ZXJzfGVufDB8MHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          title: "Starter .. ",
          id: "p7",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          img:"https://www.nonnabox.com/wp-content/uploads/Beef_Carpaccio_With_Orange_Lemon_Vinaigrette.jpg"
        },
        {
          title: "Starter .. ",
          id: "p8",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          img:"https://images.squarespace-cdn.com/content/v1/5982fa4fe58c62cb28091fa4/1574865641822-WN90VWJHZNXTIHQBH9Z5/ke17ZwdGBToddI8pDm48kFyD7pzB8zoMIVY5aiUuFlp7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0jG2lbcDYBOeMi4OFSYem8DMb5PTLoEDdB05UqhYu-xbnSznFxIRsaAU-3g5IaylIg/Miramonti2019-021.jpg"
        },
        {
          title: "Starter .. ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          img:"https://www.raymondblanc.com/wp-content/uploads/2018/04/Raymond_Blanc_001-511-1920x1080.jpg"
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
          img:"https://jackslobodian.com/wp-content/uploads/2020/03/Salmon-en-Croute-1.jpg"
        },
        {
          title: "Starter .. ",
          id: "p11",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          img:"https://cache.marieclaire.fr/data/photo/w1000_c17/cuisine/137/foiegras-joli.jpg"
        },
        {
          title: "Starter .. ",
          id: "p12",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          img:"https://static.lpnt.fr/images/2017/12/02/11500206lpw-11500210-article-jpg_4872471_1250x625.jpg"
        },
        {
          title: "Starter .. ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          img:"https://img.taste.com.au/NGH-TdgW/taste/2019/11/seafood-platter-taste-156004-2.jpg"
        },
        {
          title: "Starter .. ",
          id: "p14",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          img:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR83tCV-ssguwwczFH27CLs0tlBzJR2ZvHKzQ&usqp=CAU"
        },
        {
          title: "Starter .. ",
          id: "p15",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          img:"https://cdn.pratico-pratiques.com/app/uploads/sites/3/2019/05/30141643/tartare-de-boeuf.jpg"
        },
        {
          title: "Starter .. ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          img:"https://www.italianmade.com/usa/wp-content/uploads/2017/08/italian_made_salumi.jpg"
        },
      ]
    }
  },
}
</script>

<style scoped>

</style>