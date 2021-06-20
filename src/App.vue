<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <HelloVuex/>
  </div>
</template>

<script>
import HelloVuex from '@/components/HelloVuex.vue'

export default {
  name: 'App',
  computed: {
    message: function() {
      return this.$store.state.message
    }
  },
  components: {
    HelloVuex
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
