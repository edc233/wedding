<template>
  <div id="app">
    <div id="nav">
      <!-- 导航栏 -->
      <el-menu :default-active="activeIndex" class="el-menu" mode="horizontal" text-color='#666666' :router='true' active-text-color='#ffffff' @select="handleSelect" background-color="#000000" defaultActive='2'>
        <el-menu-item index="/">首页</el-menu-item>
        <el-menu-item index="/about">求婚套餐</el-menu-item>
        <el-menu-item index="3">求婚案例</el-menu-item>
        <el-menu-item index="4">求婚定制</el-menu-item>
        <el-menu-item index="5">求婚攻略</el-menu-item>
      </el-menu>
    </div>
    <router-view/>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: 0
    }
  },
  methods: {
    handleSelect(key, keyPath) {

    }
  },
}
</script>
<style>
  *{
    padding: 0;
    margin: 0;
  }
</style>
