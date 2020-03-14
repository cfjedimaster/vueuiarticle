<template>
  <div>
    <h3>Contact Us</h3>
    <p>
      We care a lot about what you think. Seriously. All day long I wonder - what is that random person
      on the Internet thinking about my site? So please fill the form out below so I can give your comments
      the attention they deserve!
    </p>

    <q-form>

      <q-input v-model="name" label="Your Name:" />

      <q-input v-model="email" label="Your Email:" />

      <q-select v-model="favmovie" :options="movies" label="Favorite Movie" />

      <div class="q-mt-lg">
        On my pizza I add:
        <q-option-group
          v-model="favPizzaIngredients"
          :options="pizzaIngredients"
          type="checkbox"
        />
      </div>

      <q-input label="Your Comments:" v-model="comments" type="textarea"/>

      <div class="q-mt-lg">
        <q-btn color="primary" label="Submit" />
      </div>
      
    </q-form>
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
        {label:"Peperoni", value:"Peperoni"},
        {label:"Cheese", value:"Cheese"},
        {label:"Olives", value:"Olives"},
        {label:"Sausage", value:"Sausage"},
        {label:"More Meat", value:"More Meat"},
        {label:"No Veggies", value:"No Veggies"}
      ],
      comments:''
    }
  }
}
</script>
