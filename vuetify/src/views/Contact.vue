<template>
  <div>
    <h1>Contact Us</h1>
    <p>
      We care a lot about what you think. Seriously. All day long I wonder - what is that random person
      on the Internet thinking about my site? So please fill the form out below so I can give your comments
      the attention they deserve!
    </p>

    <v-form>

      <v-text-field v-model="name" label="Your Name:" required />

      <v-text-field v-model="email" label="Your Email:" required type="email" />

      <v-select v-model="favmovie" :items="movies" label="Favorite Movie:" />

      <div>On my pizza I add:</div>
      <v-checkbox v-model="favPizzaIngredients" v-for="(ingredient,idx) of pizzaIngredients" 
      :key="idx" :label="ingredient" :value="ingredient" />

      <v-textarea v-model="comments" label="Your Comments:" outlined auto-grow="true" />

      <v-btn color="primary">Submit</v-btn>   

    </v-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name:'',
      email:'',
      favmovie:'',
      movies:[
        "Star Wars",
        "Vanilla Sky",
        "The Godfather",
        "Killer Clowns with Cats",
        "The Sound of Music"
      ],
      favPizzaIngredients:[],
      pizzaIngredients: [
        "Peperoni","Cheese","Olives","Sausage","More Meat","No Veggies"
      ],
      comments:''
    }
  }
}
</script>
