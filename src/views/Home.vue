<template>
  <div class="home">
    <h1>Homepage</h1>
    <Slider/>
<!--   <v-btn class="hidden-md-only">click</v-btn>-->
  </div>
</template>

<script>
// @ is an alias to /src
import Slider from "@/components/Slider";
export default {
  name: 'Home',
  components: {
    Slider
  }
}
</script>
