<template>
  <div>
    <home-heaer></home-heaer>
  </div>
</template>

<script>
//把子组件引入到父组件
import HomeHeaer from './components/Header'
export default {
  name: 'Home',
  //使用引入的子组件123
  components:{
    HomeHeaer
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

