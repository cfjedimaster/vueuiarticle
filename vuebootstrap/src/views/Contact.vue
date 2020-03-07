<template>
  <div>
    <h1>Contact Us</h1>
    <p>
      We care a lot about what you think. Seriously. All day long I wonder - what is that random person
      on the Internet thinking about my site? So please fill the form out below so I can give your comments
      the attention they deserve!
    </p>

    <b-form>

      <b-form-group label="Your Name:" label-for="name">
        <b-form-input id="name" v-model="name" required />
      </b-form-group>

      <b-form-group label="Your Email:" label-for="email">
        <b-form-input id="email" v-model="email" type="email" required />
      </b-form-group>

      <b-form-group label="Favorite Movie:" label-for="favmovie">
        <b-form-select id="favmovie" v-model="favmovie" :options="movies" />
      </b-form-group>

      <b-form-group label="On my pizza I add:">
        <b-form-checkbox-group v-model="favPizzaIngredients">
          <b-form-checkbox v-for="(ingredient,idx) in pizzaIngredients" :key="idx" :value="ingredient">
            {{ ingredient }}
          </b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>

      <b-form-group label="Your Comments:" label-for="comments">
        <b-form-textarea id="comments" v-model="comments" rows="3" max-rows="10" required />
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>

    </b-form>
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
