<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="row">
      <div v-for="item in list" :key="item.id" class="item">
        <div >
          {{ item }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data: () => ({
    list: [1,2,3,4,5,6,7,8,9,10]
  })
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.row {
  width: 300px;
  /* height: 50px; */
  display: flex;
  /* flex-direction: row; */
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  background-color: cadetblue
}

.item {
  height: 50px;
  width: 50px;
  background-color: antiquewhite;
  margin: 5px;
}
</style>
