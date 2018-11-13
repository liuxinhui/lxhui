<template>
    <div class="header">
        <div class="header-left"><span class="iconfont">&#xe624;</span></div>
        <div class="header-input"><span class="iconfont">&#xe632;</span>请输入内容</div>
        <div class="header-right">城市<span class="iconfont">&#xe64a;</span></div>
    </div>    
</template>
<script>
export default {
    name:'HomeHeaer',
}
</script>

<style lang='stylus' scoped>
    @import '~styles/varibles.styl'
    .header
        display :flex
        line-height :0.86rem
        background :$bgColor
        color :#fff
        .header-left
            float :left
            width :0.64rem
        .header-input
            flex :1
            background :#fff
            height .64rem
            margin-top: .12rem 
            border-radius :0.1rem
            color :#ccc
            line-height .64rem
        .header-right
            width 1rem;
            float :right 
            text-align :center       
</style>
