<template>
  <div>
    <home-heaer></home-heaer>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
//把子组件引入到父组件
import HomeHeaer from './components/Header'
import HomeSwiper from './components/swiper'
export default {
  name: 'Home',
  //使用引入的子组件123
  components:{
    HomeHeaer,
    HomeSwiper
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App12313'
    }
  }
}
</script>

