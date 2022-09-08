<template>
  <TreeChart :json="treeData" />
</template>

<script>
import TreeChart from "vue-tree-chart-3";

export default {
  name: 'app',
  components: {
    TreeChart
  },
  data() {
    return {
      landscape: [],
      treeData: {
        name: 'root',
        image_url: "https://dummyimage.com/150x150/ccc/999.png&text=root",
        children: [
          {
            name: 'children1',
            image_url: "https://dummyimage.com/150x150/ccc/999.png&text=children1"
          },
          {
            name: 'children2',
            image_url: "https://dummyimage.com/150x150/ccc/999.png&text=children2",
            mate: [{
              name: 'mate',
              image_url: "https://dummyimage.com/150x150/ccc/999.png&text=mate"
            }],
            children: [
              {
                name: 'grandchild',
                image_url: "https://dummyimage.com/150x150/ccc/999.png&text=grandchild"
              },
              {
                name: 'grandchild2',
                image_url: "https://dummyimage.com/150x150/ccc/999.png&text=grandchild2"
              },
              {
                name: 'grandchild3',
                image_url: "https://dummyimage.com/150x150/ccc/999.png&text=grandchild3"
              }
            ]
          },
          {
            name: 'children3',
            image_url: "https://dummyimage.com/150x150/ccc/999.png&text=children3"
          }
        ]
      }
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
