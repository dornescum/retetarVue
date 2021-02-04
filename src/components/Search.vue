<template>
<!--  <v-text-field ref="search"-->
<!--                label="Search ..."-->
<!--                :rules="rules"-->
<!--                hide-details="auto"-->
<!--                width="400px"-->
<!--                @click="resetSearch"-->
<!--  >-->
<!--    <v-icon-->
<!--        slot="append"-->
<!--        color="grey"-->
<!--        @click="submitSearch"-->

<!--    >-->
<!--      mdi-plus-->
<!--    </v-icon>-->
<!--  </v-text-field>-->

  <input @click.enter="resetSearch" placeholder="search ..." class="input-box">
<!--  <p>Message is: {{ message }}</p>-->
</template>

<script>
export default {
  name: "Search",
  data: () => ({
    // message : " ",
    search: "",
    // rules: [
    //   value => !!value || 'Required..',
    //   value => (value && value.length >= 3) || 'Min 3 characters',
    // ],
  }),
  methods: {

  //   submitSearch() {
  //
  //     if (this.$refs.search.validate()) {
  //       console.log(this.$refs.search)
  //       this.$refs.search.reset()
  //     }
  //   },
    resetSearch() {
      // setTimeout(()=> this.search = " ", 1000)
      setTimeout(this.search = null, 1000)

    }
  }
}
</script>

<style scoped>
.input-box{
  border: 1px solid lightgray;
  border-radius: 7px;
  padding-left: 15px;
}
@media (max-width: 768px){
  .input-box{
    width: 100px;
    padding: 5px 0 5px 15px;
    /*padding: 0;*/
    /*display: none;*/
  }
}


</style>