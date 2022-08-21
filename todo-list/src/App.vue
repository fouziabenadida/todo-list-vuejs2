<template>
  <div id="app">
  <header-todo></header-todo>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
   'header-todo': Header
  }
}
</script>

<style>

</style>
