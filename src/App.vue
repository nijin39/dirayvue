<template>
  <div id="app">
    <el-menu :default-active="activeIndex" :router="true" class="el-menu-demo" mode="horizontal" @select="handleSelect">
  <el-menu-item index="1" :route="{name:'HelloWorld'}">Processing Center</el-menu-item>
  <el-submenu index="2">
    <template slot="title">Workspace</template>
<el-menu-item index="2-1">item one</el-menu-item>
<el-menu-item index="2-2">item two</el-menu-item>
<el-menu-item index="2-3">item three</el-menu-item>
</el-submenu>
<el-menu-item index="3" :route='{path:"/test"}' >Orders</el-menu-item>
</el-menu>

<!--<img src="./assets/logo.png">-->
<router-view/>
</div>
</template>

<script>
  export default {
    name: 'app',
    data () {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      }
    },
    methods: {
      handleSelect (key, keyPath) {
        console.log(key, keyPath)
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
  }
</style>
