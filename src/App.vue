<template>
  <div id="app">
    <el-container class="cm-container">
      <el-aside width="auto">
        <gh-menu></gh-menu>
      </el-aside>
      <el-container>
        <el-header>
          <gh-header></gh-header>
        </el-header>
        <el-main>
          <div class="block">
            <el-button type="primary" icon="el-icon-edit" />
            <el-button type="primary" icon="el-icon-share" />
            <el-button type="primary" icon="el-icon-delete" />
            <el-button type="primary" icon="el-icon-search">Search</el-button>
            <el-button type="primary">
              Upload
              <i class="el-icon-upload el-icon-right" />
            </el-button>
          </div>
            <el-link disabled>默认链接</el-link>
  <el-link type="primary" disabled>主要链接</el-link>
  <el-link type="success" disabled>成功链接</el-link>
  <el-link type="warning" disabled>警告链接</el-link>
  <el-link type="danger" disabled>危险链接</el-link>
  <el-link type="info" disabled>信息链接</el-link>
          <!-- <router-view /> -->
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    ghMenu: () => import('@/components/ghMenu'),
    ghHeader: () => import('@/components/ghHeader')
  }
}
</script>
<style>
* {
  margin: 0;
  padding: 0;
  border: 0;
}
</style>
<style lang="scss" scoped>
@import "./sass/variables";

#app {
  max-width: 100vw;
  min-height: 100vh;

  .cm-container {
    height: 100%;

    .el-aside {
      min-height: 100vh;
      background: $backgrond;
    }
    .el-header {
      height: auto;
      padding: 0;
      box-sizing: border-box;
    }
  }
}
</style>
