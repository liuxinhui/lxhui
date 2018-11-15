<template>
    <div>
        <div class="title">周末游</div>
        <ul>
            <li class="item" v-for="item of recomentList" :key='item.id'>
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="华宇" />
                </div>    
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>    
            </li>
        </ul>    
    </div>
</template>

<script>
    export default {
        name:'WeedTravel',
        data (){
            return {
                recomentList:[{
                    id:'001',
                    imgUrl:'https://img1.qunarzz.com/des-mis/ad/1810/1c/cea3dc3af5cb95.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'002',
                    imgUrl:'https://img1.qunarzz.com/des-mis/ad/1810/1c/cea3dc3af5cb95.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'003',
                    imgUrl:'https://img1.qunarzz.com/des-mis/ad/1810/1c/cea3dc3af5cb95.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'004',
                    imgUrl:'https://img1.qunarzz.com/des-mis/ad/1810/1c/cea3dc3af5cb95.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                }]
            }
        },
        methods:{
            handleClick(item){
                console.log(item)
            }
        }
    }
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
