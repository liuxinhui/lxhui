<template>
  <div>
    <home-heaer></home-heaer>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recoment></home-recoment>
    <Weed-travel></Weed-travel>
  </div>
</template>

<script>
//把子组件引入到父组件
import HomeHeaer from './components/Header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeRecoment from './components/Recoment'
import WeedTravel from './components/Weedtravel'
export default {
  name: 'Home',
  //使用引入的子组件123
  components:{
    HomeHeaer,
    HomeSwiper,
    HomeIcons,
    HomeRecoment,
    WeedTravel
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App12313'
    }
  }
}
</script>

