<template>
  <div>

    <h1>Pictures of our Cats</h1>


      <v-container fluid>
          <v-row>
            <v-col v-for="(cat, idx) of cats" cols="4" :key="idx">
              <v-img :src="cat" height="300" max-height="350" />
            </v-col>
          </v-row>
      </v-container>
  </div>
</template>


<script>

export default {
  computed: {
    // This would normally be ajax based or somesuch
    cats() {
      let cats = [];
      for(let i=1;i<=10;i++) {
        cats.push(`/images/cats/cat${i}.jpg`);
      }
      return cats;
    }
  }
}
</script>