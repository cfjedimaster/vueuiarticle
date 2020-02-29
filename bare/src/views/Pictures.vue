<template>
  <div>
    <h1>Pictures of our Cats</h1>

    <img v-for="(cat, idx) of cats" :src="cat" :key="idx" />
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