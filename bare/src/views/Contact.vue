<template>
  <div>
    <h1>Contact Us</h1>
    <p>
      We care a lot about what you think. Seriously. All day long I wonder - what is that random person
      on the Internet thinking about my site? So please fill the form out below so I can give your comments
      the attention they deserve!
    </p>

    <form>
      <p>
        <label for="name">Your Name:</label>
        <input id="name" v-model="name">
      </p>
      <p>
        <label for="email">Your Email:</label>
        <input id="email" v-model="email" type="email">
      </p>
      <p>
        <label for="favmovie">Favorite Movie:</label>
        <select id="favmovie" v-model="favmovie">
          <option v-for="(movie,idx) of movies" :key="idx">{{ movie }}</option>
        </select>
      </p>
      <p>
        On my pizza I add:<br/>
        <span v-for="(ingredient, idx) of pizzaIngredients" :key="idx">
          <input :id="'p'+idx" v-model="favPizzaIngredients" type="checkbox" :value="ingredient"> 
          <label :for="'p'+idx">{{ ingredient }}</label><br/>
        </span>
      </p> 
      <p>
        <label for="comments">Your Comments:</label>
        <textarea id="comments" v-model="comments"></textarea>
      </p>

      <p>
        <input type="submit">
      </p>
      
    </form>
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
