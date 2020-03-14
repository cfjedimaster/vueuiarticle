<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="glossy">
      <q-toolbar>

        <q-toolbar-title>
          UI Demo
        </q-toolbar-title>

        <q-tabs>
          <q-route-tab to="/" label="Home" />
          <q-route-tab to="/cats" label="Cats"  />
          <q-route-tab to="/pics" label="Pictures" />
          <q-route-tab to="/contact" label="Contact" />
        </q-tabs>

      </q-toolbar>
    </q-header>
   
    <q-page-container class="q-pa-md">
      <router-view></router-view>
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'LayoutDefault',

  components: {
  },

  data () {
    return {
    }
  }
}
</script>

<style>
</style>
