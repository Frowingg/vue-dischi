<template>
  <div id="app">
    <header>
      <img src="./assets/logo.png" alt="">

      <selectGenre />

    </header>

    <main>
      <CdListComponent />
    </main>

  </div>
</template>

<script>
import CdListComponent from './components/CdListComponent.vue';
import selectGenre from './components/selectGenre.vue';


export default {
  name: 'App',
  components: {
    CdListComponent,
    selectGenre
}
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
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
  height: 40px;
  display: flex;
  justify-content: space-between;
}
header img{
  width: 20px;
  height: 20px;
}
main{
  background-color: #1e2d3b;
  height: calc(100vh - 40px);
}
</style>
