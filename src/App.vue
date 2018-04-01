<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <input v-model="origin" placeholder="edit me">
    <circle-container v-bind:height="100" v-bind:width="100" v-bind:text="origin"></circle-container>
    <circle-container v-bind:height="200" v-bind:width="200" v-bind:text="origin"></circle-container>
  </div>
</template>

<script>
import Circle from './components/circle.vue';

export default {
  name: 'app',

  components: {'circle-container': Circle},

  data () {
    return {
      msg: 'Test project',
      origin: ''
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
