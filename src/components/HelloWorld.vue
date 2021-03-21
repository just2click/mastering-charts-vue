<template>
  <div class="hello">
    <v-chart v-bind:chartData="setLinearGraphData"></v-chart>
    <v-chart v-bind:chartData="setLinearGraphData2"></v-chart>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['id', 'data'],
  data () {
    return {
      chartData: {
        chartType: 'lineGraph',
        selector: 'chart',
        title: 'Student Grades',
        subtitle: '2018 - 2019',
        metric: ['value'],
        dim: 'time',
        label: true,
        width: 600,
        height: 300,
        data: []
      },
      chartData2: {
        chartType: 'lineGraph',
        selector: 'chart2',
        title: 'Test Values',
        subtitle: '2018 - 2019',
        metric: ['value'],
        dim: 'time',
        label: true,
        width: 600,
        height: 300,
        data: []
      }
    }
  },
  computed: {
    setLinearGraphData () {
      this.setData()
      return this.chartData
    },
    setLinearGraphData2 () {
      this.setData2()
      return this.chartData2
    }
  },
  methods: {
    setData () {
      this.chartData.data = this.data
    },
    setData2 () {
      this.chartData2.data = this.data
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
