<template>
  <v-container>
    <v-carousel id="picture">
      <v-carousel-item
          v-for="item in items"
          :key="item.src"
          :src="item.src"
      ></v-carousel-item>
    </v-carousel>
  </v-container>
</template>

<script>
export default {
name: "Slider",
  data () {
    return {
      items: [
        {
          src:"https://images.unsplash.com/photo-1498837167922-ddd27525d352?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8Zm9vZHxlbnwwfDB8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
        },
        {
          src: 'https://images.pexels.com/photos/406152/pexels-photo-406152.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500',
        },
        {
          src: 'https://images.pexels.com/photos/1640777/pexels-photo-1640777.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500',
        },
        {
          src: '../assets/logo.png',
        },
      ],
    }
  },
}
</script>

<style>
#picture{
  height: 600px !important;
  background-image: url("../assets/logo.png");
}
</style>