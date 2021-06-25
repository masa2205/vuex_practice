<template>
  <div id="app">
    <p>
      <button @click="increment">UP</button>
    </p>
    <h2>Count:{{ count }}</h2>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    increment : function() {
      this.$store.dispatch('incrementOne')
    }
  },
  computed: {
    count : function(){
      return this.$store.state.count
    }
  },
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
