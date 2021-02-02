<template>
  <v-app class="grey">
    <Navbar/>
    <v-main>
     <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from "@/components/UI/Navbar";
export default {
  name: 'App',

  components: {
Navbar
  },

  data: () => ({
    //
  }),
};
</script>
<style>
.red{
  background-color: red;
}
</style>
