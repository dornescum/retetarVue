<template>
  <v-dialog v-model="dialog" width="500">
    <template v-slot:activator="{ on }">
      <v-btn class="grey lighten-1" dark v-on="on">Add new recipe</v-btn>
    </template>
    <v-card>
      <v-card-title class="headline grey lighten-2" primary-title>Add a new recipe</v-card-title>
    </v-card>
    <v-card-text>
      <v-form class="px-3">
        <v-text-field label="Title of the recipe" v-model="title" prepend-icon="mdi-silverware-fork-knife"></v-text-field>
        <v-textarea label="recipe" v-model="recipe" prepend-icon="mdi-silverware-fork-knife"></v-textarea>
        <v-btn class="error mx-3 mt-3" @click="submitRecipe"> add </v-btn>
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
      recipe:""
    }
  },
  methods:{
    submitRecipe(){
      console.log(this.title, this.recipe)
    }
  }
}
</script>

<style scoped>

</style>