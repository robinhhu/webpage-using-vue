<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">HOME</router-link> &nbsp; | &nbsp;
      <router-link to="/Pic">构建企业全息画像</router-link> &nbsp; | &nbsp;
      <router-link to="/two">僵尸企业识别分类</router-link>
    </div>
    <router-view/>
    <!-- <Home/> -->
  </div>
</template>

<script>
// import Home from './views/Home.vue'

export default {
  components: {
    // Home
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
  }

  #nav {
    padding: 1.3vw;
    font-size: 1.2vw;
    background-color: #f8f8f8;
    border-color: #e7e7e7;
    text-align: left;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;
  }

  #nav a.router-link-exact-active {
    color:#669;
  }
</style>
