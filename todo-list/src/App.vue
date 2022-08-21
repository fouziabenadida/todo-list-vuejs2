<template>
  <div id="app">
  <header-todo></header-todo>
  <tache-a-faire></tache-a-faire>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Tache from './components/Tache.vue'

export default {
  name: 'App',
  components: {
   'header-todo': Header,
   'tache-a-faire': Tache

  }
}
</script>

<style>

</style>
