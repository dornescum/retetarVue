<template>
  <v-app class="grey">
    <Navbar/>
    <v-main>
      <router-view></router-view>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Navbar from "@/components/UI/Navbar";
import Footer from "@/components/UI/Footer";

export default {
  name: 'App',

  components: {
    Navbar,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
<style>
.red {
  background-color: red;
}
</style>
