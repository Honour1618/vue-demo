<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{ totalPrice }}
    <apple></apple>
    <banana></banana>
    
    <!--
    <ransition name="fade">
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </ransition>

     简单跳转直接使用to (前面加个/,/apple，跳至根目录)
    <router-link to="apple">to apple</router-link>
    <router-link :to="{name:'applePage'}">to apple</router-link>
    
    <router-link :to="'/apple'" tag="li">to apple</router-link>
    <router-link :to="{path:'applePage'}">to banana</router-link>
    <router-link :to="{path:'apple/red'}">to apple red</router-link>
    -->
    
  </div>
</template>

<script>
import Apple from './components/apple'
import Banana from './components/banana'
export default {
  components:{Apple, Banana},
  computed: {
    totalPrice () {
      return this.$store.getters.getTotal
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
  margin-top: 60px;
}
</style>
