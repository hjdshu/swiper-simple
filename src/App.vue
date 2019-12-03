<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <div class="banner">
      <Swiper>
        <swiper-item>1</swiper-item>
        <swiper-item>2</swiper-item>
        <swiper-item>3 </swiper-item>
      </Swiper>
    </div>

    <div class="one" ref="oneclick">一次</div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import {Swiper, SwiperItem} from './components/swiper-simple'
import { once } from 'wind-dom/src/event'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    Swiper,
    SwiperItem
  },
  mounted () {
    once(this.$refs.oneclick, 'click', function(){
      alert(1)
    })
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
.banner{
  margin: 0 auto;
  background: rgb(17, 57, 141);
  width: 200px;
  height: 100px;
  color: #fff;
}
</style>
