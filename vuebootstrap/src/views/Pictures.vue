<template>
  <div>
    <h1>Pictures of Our Cats</h1>
    
    <b-container>
      <b-row align-v="center" align-h="center">
        <b-col cols="4" v-for="(cat, idx) of cats" :key="idx">
          <img :src="cat" class="img-thumbnail img-fluid m-4" />
        </b-col>
      </b-row>
    </b-container>

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

<style scoped>
img {
  max-width: 250px;
  max-height: 250px;
}
</style>