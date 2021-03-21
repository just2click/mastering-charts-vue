<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello-world :data="data" :id="g1" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  components: { HelloWorld },
  name: 'App',
  data () {
    return {
      data: [
        {
          time: 0.5,
          value: 75
        },
        {
          time: 1,
          value: 15
        },
        {
          time: 1.5,
          value: 90
        },
        {
          time: 2,
          value: 30
        },
        {
          time: 2.5,
          value: 10
        },
        {
          time: 3,
          value: 99
        },
        {
          time: 3.5,
          value: 10
        },
        {
          time: 4,
          value: 96
        },
        {
          time: 4.5,
          value: 79
        },
        {
          time: 5,
          value: 10
        },
        {
          time: 6,
          value: 90
        },
        {
          time: 6.5,
          value: 10
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
