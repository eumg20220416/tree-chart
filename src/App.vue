<template>
  <TreeChart :json="treeData" />
</template>

<script>
import TreeChart from "vue-tree-chart-3";
import axios from "axios";

export default {
  name: 'app',
  components: {
    TreeChart
  },
  data() {
    return {
      landscape: [],
      treeData: {}
    }
  },
  mounted() {
    axios.get('./data/treedata.json')
    .then(response => this.treeData = response.data)
    .catch(error => console.log(error))
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
