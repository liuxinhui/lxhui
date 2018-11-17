<template>
  <div>
    <home-heaer></home-heaer>
    <home-swiper :list="swiperList"></home-swiper>
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
import axios from 'axios'
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
      swiperList:[]
    }
  },
  methods:{
    getHomeInfo(){
      axios.get('../../../static/mock/index.json')
      .then(this.getInfo)
    },
    getInfo(res){
      console.log(res)
      res = res.data
      if(res.ret && res.data){
        const data = res.data
        this.swiperList = data.swiperList
      }
    }
  },
  mounted (){
    this.getHomeInfo()
  }
}
</script>

