<template>
  <div>
    <h3>Pictures of our Cats</h3>

    <div class="row">
      <div class="col-3"></div>
      <div class="col-6">
        <q-carousel animated arrows navigation v-model="slide" class="q-ma-lg">
        <q-carousel-slide v-for="(cat, idx) of cats" :img-src="cat" :key="idx" :name="idx" />
        </q-carousel>
      </div>
      <div class="col-3"></div>
    </div>
  </div>
</template>


<script>

export default {
  data() {
    return {
      slide: 0
    }
  },
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