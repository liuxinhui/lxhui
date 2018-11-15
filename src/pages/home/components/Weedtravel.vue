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
                    <button class="item-button" @click="handleClick">查看详情</button>
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
                    imgUrl:'http://pic.dominos.com.cn:8000/ApiPicture/ECManager/20180918/13890ff66898426489756d2e7da1cab5.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'002',
                    imgUrl:'http://pic.dominos.com.cn:8000/ApiPicture/ECManager/20180918/13890ff66898426489756d2e7da1cab5.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'003',
                    imgUrl:'http://pic.dominos.com.cn:8000/ApiPicture/ECManager/20180918/13890ff66898426489756d2e7da1cab5.jpg',
                    name:'华宇',
                    title:'北京华宇信息有限公司',
                    desc:'xxxxxx'
                },{
                    id:'004',
                    imgUrl:'http://pic.dominos.com.cn:8000/ApiPicture/ECManager/20180918/13890ff66898426489756d2e7da1cab5.jpg',
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
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
