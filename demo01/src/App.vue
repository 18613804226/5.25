<template>
  <div id="app">
    <router-view />
    <tabar></tabar>
  </div>
</template>

<style lang='less'>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  font-size: 13px;
}
*{
  margin: 0;
  padding: 0;
}
</style>
<script>
  import {obj} from './utils';
  import tabar from "../src/components/tabar";
export default {
  mounted() {
    obj.setRem()
  },
  components: {
    tabar
  }
}
</script>