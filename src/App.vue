<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <header>
      <img src="./assets/logo.png" alt="">
    </header>

    <main>

    </main>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
header{
  background-color: #2e3a46;
  padding: 10px 15px;
  height: 60px;
}
header img{
  width: 40px;
  height: 40px;
}
main{
  background-color: #1e2d3b;
  height: calc(100vh - 60px);
}
</style>
