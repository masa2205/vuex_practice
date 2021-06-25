<template>
  <div id="app">
    <h1>ユーザ一覧</h1>
    <div v-for="user in users" :key=user.id>{{user.name}}</div>
  </div>
</template>

<script>
export default {
  name: 'App',
  computed: {
    users : function(){
      return this.$store.state.users
    }
  },
  mounted(){
    this.$store.dispatch('getUsers')
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
