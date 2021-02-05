<template>
  <v-dialog v-model="dialog" width="500">
    <template v-slot:activator="{ on }">
      <v-btn class="grey lighten-1 ml-6"   dark v-on="on" >Add your recipe</v-btn>
    </template>
    <v-card>
      <v-card-title class="headline grey lighten-2" primary-title>Add a new recipe</v-card-title>
    </v-card>
    <v-card-text class="grey lighten-3">
      <v-form class="px-3" ref="form">
        <v-text-field label="Title of the recipe" v-model="title" prepend-icon="mdi-silverware-fork-knife"
                      :rules="inputRules"
        ></v-text-field>
        <v-textarea label="recipe" v-model="recipe" prepend-icon="mdi-silverware-fork-knife"  :rules="inputRules"></v-textarea>
        <v-btn class="error mx-3 mt-3" @click="submitRecipe" :loading="loading"  :disabled="loading"> add </v-btn>
      </v-form>
    </v-card-text>
  </v-dialog>

</template>

<script>
export default {
  name: "Dialog",
  data(){
    return{
      title:"",
      recipe:"",
      loader: null,
      dialog: null,
      inputRules: [
          // v => v.length >=3 || "Minimum length is 3 characters"
        v =>  v && v.length >= 3 || 'Minimum length is 3 characters'
      ],
      loading: false
    }
  },
  methods:{
    submitRecipe(){
     // if (this.$ref.form.validate()) {
     //   console.log(this.title, this.recipe)
     // }
      if(this.$refs.form.validate()){
        console.log(this.title, this.recipe)
        this.$refs.form.reset()
      }

    }
  },
  // watch: {
  //   loader () {
  //     const l = this.loader
  //     this[l] = !this[l]
  //
  //     setTimeout(() => (this[l] = false), 3000)
  //
  //     this.loader = null
  //   },
  // },
}
</script>

<style scoped>

</style>