<template>
  <div id="app">

    <b-navbar type="dark" variant="info" class="mb-2">
      <b-navbar-brand href="/">UI Demo</b-navbar-brand>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/cats" :active="thisRoute == 'Cats'">Cats</b-nav-item>
          <b-nav-item to="/pics" :active="thisRoute == 'Pictures'">Pictures</b-nav-item>
          <b-nav-item to="/contact" :active="thisRoute == 'Contact'">Contact</b-nav-item>
        </b-navbar-nav>

      </b-collapse>
    </b-navbar>

    <router-view/>
  </div>
</template>

<script>
export default {
  computed: {
    thisRoute() {
      return this.$route.name;
    }
  }
}
</script>

<style scoped>
#app {
  margin: 20px;
}
</style>