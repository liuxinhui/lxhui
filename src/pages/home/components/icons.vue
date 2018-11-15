<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page, index) of pages" :key="index">
                <div class="icon" v-for="item in page" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl">
                        <p class="icon-desc">{{item.desc}}</p>
                    </div>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name:'HomeIcons',
    data (){
        return {
            iconList:[{
                id:'0001',
                imgUrl:'https://fuss10.elemecdn.com/e/c7/b7ba9547aa700bd20d0420e1794a8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'景点门票大撒大大大阿萨达v'
            },{
                id:'0002',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'华宇信息'
            },{
                id:'0003',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'3'
            },{
                id:'0004',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'4'
            },{
                id:'0005',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'5'
            },{
                id:'0006',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'6'
            },{
                id:'0007',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'7'
            },{
                id:'0008',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'8'
            },{
                id:'0009',
                imgUrl:'https://fuss10.elemecdn.com/c/21/e42997b86b232161a5a16ab813ae8jpeg.jpeg?imageMogr/format/webp/thumbnail/!90x90r/gravity/Center/crop/90x90/',
                desc:'9'
            }]
        }
    },
    computed :{
        pages () {
        const pages = []
        this.iconList.forEach((item, index) => {
            const page = Math.floor(index / 8)
            if (!pages[page]) {
            pages[page] = []
            }
            pages[page].push(item)
        })
        return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
   .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center 
        color :black
        ellipsis()
</style>