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
          favorite: true,
          chef: "Ionel B",
          url: "/starters",
          img:"https://avatars.mds.yandex.net/get-zen_doc/3618266/pub_5f295b02167fe43864d71c20_5f295b05081b6d0ad0b5395b/scale_1200"
        },
        {
          title: "Recomandations .. ",
          id: "p2",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 2123,
          favorite: true,
          chef: "Ionel B",
          img:"https://www.businesstraveller.com.ru/upload/medialibrary/b21/b2140a0e0d6aa7789afda66e4cfbde73.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p3",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 523,
          favorite: true,
          chef: "Gigi V.",
          img:"https://cstor.nn2.ru/forum/data/forum/images/2018-01/195844418-best_rest_4.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p4",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.5,
          reviews: 723,
          favorite: true,
          chef: "Marian P",
          img:"https://gbc-cdn-public-media.azureedge.net/img11506.1426x713.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p5",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 623,
          favorite: true,
          chef: "Gigi R",
          img:"https://old.gastronomic.ru/uploads/places/thumb_place_1144_step_8549_1584219722_upto_1024_x_768.jpeg"
        },
        {
          title: "Recomandations .. ",
          id: "p6",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.8,
          reviews: 3,
          favorite: true,
          chef: "Angela B",
          img:"https://storage.ginzadelivery.ru/product/18562/l.0389288fd08dbd7809604c7eaf85fdd0.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p7",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.9,
          reviews: 43,
          favorite: true,
          chef: "Vasilica B",
          img:"https://make-eat.ru/sushi-rollu-souse-news/2034.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p8",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.5,
          reviews: 89,
          favorite: true,
          chef: "Ionel B",
          img:"https://komuzhitkhorosho.ru/wp-content/uploads/2017/06/DSC_8254-1024x683.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p9",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 1.5,
          reviews: 103,
          favorite: true,
          chef: "Ionel B",
          img:"https://img-global.cpcdn.com/recipes/5c821ab3df88f4c9/1502x1064cq70/stieik-iz-lososia-s-sousom-iz-shampanskogho-s-ikroi-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D0%BE%D0%B5-%D1%84%D0%BE%D1%82%D0%BE-%D1%80%D0%B5%D1%86%D0%B5%D0%BF%D1%82%D0%B0.jpg"
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
          img:"https://old.gastronomic.ru/uploads/places/thumb_place_1607_step_7905_1570998072_upto_1024_x_768.jpeg"
        },
        {
          title: "Recomandations .. ",
          id: "p11",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.5,
          reviews: 13,
          favorite: true,
          chef: "Ionela S",
          img:"https://avatars.mds.yandex.net/get-altay/1684282/2a0000016a6d968bb5a6e54395c229a409f5/XXL"
        },
        {
          title: "Recomandations .. ",
          id: "p12",
          type: "vegetarian",
          text: "See the recipe here",
          value: 3.8,
          reviews: 24,
          favorite: true,
          chef: "Mariana B",
          img:"https://i.pinimg.com/originals/29/2a/69/292a695b263bb7118feed5ce41907c11.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p13",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 3.9,
          reviews: 2234,
          favorite: true,
          chef: "Ionel B",
          img:"https://stpetersburg4you.com/wp-content/uploads/2017/01/r5.gif"
        },
        {
          title: "Recomandations .. ",
          id: "p14",
          type: "vegetarian",
          text: "See the recipe here",
          value: 2.8,
          reviews: 2235,
          favorite: true,
          chef: "Ionel B",
          img:"https://www.bigonioncaterer.com.my/wp-content/uploads/2018/03/HOME-1.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p15",
          type: "vegetarian",
          text: "See the recipe here",
          value: 4.2,
          reviews: 213,
          favorite: true,
          chef: "Gigina B",
          img:"https://i.ytimg.com/vi/l1dQEZWI-gs/maxresdefault.jpg"
        },
        {
          title: "Recomandations .. ",
          id: "p16",
          type: "non-vegetarian",
          text: "See the recipe here",
          value: 4.3,
          reviews: 293,
          favorite: true,
          chef: "Ionel B",
          img:"https://www.afisha.ru/uploads/3/05/305bcf20c3c44b36aa72a7c35588289c.jpg"
        },

      ]
    }
  },
}
</script>

<style scoped>

</style>