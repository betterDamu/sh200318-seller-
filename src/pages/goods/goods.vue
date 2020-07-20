<template>
    <div class="goodsWrap">
        <div class="goods">
            <div class="left" ref="left">
                <ul class="typeList">
                    <li class="typeItem" v-for="(good,index) in goods" :key="index">
                        <seller-icon class="icon" size="3"
                          v-show="good.type >= 0"  :type="good.type"></seller-icon>
                        <span class="name">{{good.name}}</span>
                    </li>
                </ul>
            </div>
            <div class="right"></div>
        </div>
        <div class="cart"></div>
    </div>
</template>

<script>
    import {mapState} from "vuex";
    import BScroll from 'better-scroll'
    export default {
        name: "goods",
        computed:{
            ...mapState(["goods","iconTypes"])
        },
        mounted(){
             //将滑屏的包裹器传入到BScroll内部就可以产生滑屏
             new BScroll(this.$refs.left)
        }
    }
</script>

<style scoped lang="stylus">
@import "../../common/stylus/mixin.styl"
.goodsWrap
    display flex
    flex-direction column
    .goods
        flex 1
        display flex
        overflow hidden
        .left
            width 80px
            .typeList
                .typeItem
                    one-px(rgba(7,17,27,.1))
                    display flex
                    justify-content center
                    align-items center
                    box-sizing border-box
                    width 80px
                    height 54px
                    padding 0 12px
                    background #f3f5f7
                    font-size:12px
                    line-height 14px
                    color rgba(0,0,0,.6)
                    font-weight bold
                    &:after
                        width 56px
                    &:last-child
                        border-none()
                    .icon
                        margin-right 3px
                    .name
                        zoom 1
        .right
            flex 1
            background pink
    .cart
        height 46px
        background gray
</style>