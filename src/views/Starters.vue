<template>
<div>

 <v-container>
   <v-row>
     <v-col id="test"
         v-for="item in pasta"
         :key="item.id"
         cols="12"
         sm="6"
         lg="4"

     >

       <v-flex>
         <v-app id="inspire">
           <v-card
               :loading="loading"
               class="mx-auto my-0"
               max-width="374"
               min-height="60px"
           >
             <template slot="progress">
               <v-progress-linear
                   color="deep-purple"
                   height="10"
                   indeterminate
               ></v-progress-linear>
             </template>

             <v-img
                 height="250"
                 src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
             ></v-img>

             <v-card-title>Cafe Badilico</v-card-title>

             <v-card-text>
               <v-row
                   align="center"
                   class="mx-0"
               >
                 <v-rating
                     :value="4.5"
                     color="amber"
                     dense
                     half-increments
                     readonly
                     size="14"
                 ></v-rating>

                 <div class="grey--text ml-1">
                   4.5 (413)
                 </div>
               </v-row>

               <div class="my-4 subtitle-1">
                 $ • Italian, Cafe
               </div>

               <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
             </v-card-text>

             <v-divider class="mx-4"></v-divider>

             <v-card-title>Tonight's availability</v-card-title>

             <v-card-text>
               <v-chip-group
                   v-model="selection"
                   active-class="deep-purple accent-4 white--text"
                   column
               >
                 <v-chip>5:30PM</v-chip>

                 <v-chip>7:30PM</v-chip>

                 <v-chip>8:00PM</v-chip>

                 <v-chip>9:00PM</v-chip>
               </v-chip-group>
             </v-card-text>

             <v-card-actions>
               <v-btn
                   color="deep-purple lighten-2"
                   text
                   @click="reserve"
               >
                 Reserve
               </v-btn>
             </v-card-actions>
           </v-card>
         </v-app>

       </v-flex>





     </v-col>
   </v-row>
 </v-container>
</div>
</template>

<script>
export default {
name: "Starters",
  data: () => ({
    loading: false,
    selection: 1,
    pasta: [
      {
        title: "pasta 1",
        id: "p1",
        ingredients: "bla, bla",
        text: "description of the recipe",
        img: "https://images.unsplash.com/photo-1604382354936-07c5d9983bd3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
        favorite: true
      },
      {
        title: "pasta 2",
        id: "p2",
        ingredients: "bla, bla, onion",
        text: "description",
        img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",
        favorite: false
      },
      {
        title: "pasta 3",
        id: "p3",
        text: "description",
        img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",

        favorite: false
      },
      {
        title: "pasta 4",
        id: "p4",
        text: "description",
        img:"https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=925&q=80",

        favorite: false
      },

    ],
  }),

  methods: {
    reserve () {
      this.loading = true

      setTimeout(() => (this.loading = false), 2000)
    },
  },
}
</script>

<style scoped>
#test{
  min-height: 10vh;
}
</style>