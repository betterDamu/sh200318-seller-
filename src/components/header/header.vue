<template>
    <div class="seller_header">
        <div class="top">
            <div class="top_left">
                <img class="avatar"
                     src="https://fuss10.elemecdn.com/8/40/02872ce8aefe75c16d3190e75ad61jpeg.jpeg">
            </div>
            <div class="top_right">
                <div class="title">
                    <i class="brand"></i>
                    <span class="name">茄子哥(方舟园)</span>
                </div>
                <div class="delivery">
                    <span class="info">蜂鸟专送/38分钟送达</span>
                </div>
                <div class="supports">
                    <seller-icon class="icon" size="3" type="special"></seller-icon>
                    <span class="text">在线支付满25送店;满50送老板</span>
                </div>
            </div>
            <div class="btns">
                <span class="count">5个</span>
                <i class="seller-keyboard_arrow_right arrow_right"></i>
            </div>
        </div>
        <div class="bottom">
            <i class="icon"></i>
            <span class="text">
                是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
            </span>
            <i class="seller-keyboard_arrow_right arrow_right"></i>
        </div>
        <div class="bg">
            <img src="https://fuss10.elemecdn.com/8/40/02872ce8aefe75c16d3190e75ad61jpeg.jpeg">
        </div>
        <div class="mask">
            <div class="contentWrap">
                <div class="content">
                    <!--真正的遮罩内容-->
                    <div class="title">
                        <span>茄子哥(方舟园店)</span>
                    </div>
                    <div class="stars"></div>
                    <seller-line class="line">
                        <span>优惠信息</span>
                    </seller-line>
                    <seller-list></seller-list>
                    <seller-line class="line">
                        <span>商家公告</span>
                    </seller-line>
                    <p class="bulletin">
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                        是以粥为特色的中式营养快餐，自2004年10月18日创立“嘉和一品”品牌至今，不断优化管理，积极创新，立足于“贴近百姓生活，服务千家万户”
                    </p>
                </div>
            </div>
            <div class="footer">
                <i class="seller-close close"></i>
            </div>
        </div>
    </div>
</template>

<script>
    import list from "components/list/list.vue"
    export default {
        name: "seller-header",
        components:{
            "seller-list":list
        }
    }
</script>

<style scoped lang="stylus">
    @import "../../common/stylus/mixin.styl"
    @import "../../common/stylus/extend.styl"
    .seller_header
        background rgba(7,17,27,.5)
        position relative
        & > .top
            padding 24px 12px 18px 24px
            display flex
            position relative
            .top_left
                width 64px
                height 64px
                margin-right 16px
                .avatar
                    width 100%
                    height 100%
            .top_right
                color rgba(255,255,255,1)
                .title
                    display flex
                    align-items center
                    font-size 16px
                    font-weight bold
                    line-height 18px
                    margin-top 2px
                    margin-bottom 8px
                    .brand
                        bg-image(brand)
                        background-repeat no-repeat
                        background-size 100%
                        display inline-block
                        width 30px
                        height 18px
                    .name
                        margin-left 6px
                .delivery
                    font-size 12px
                    font-weight 200
                    line-height 12px
                    .info
                        zoom 1
                .supports
                    display flex
                    align-items center
                    font-size 10px
                    font-weight 200
                    line-height 12px
                    margin-top 10px
                    margin-bottom 2px
                    .text
                        margin-left 4px
                    .icon
                        zoom 1
            .btns
                position absolute
                right 12px
                bottom 12px
                width 45px
                height 24px
                background rgba(0,0,0,0.2)
                font-size 10px
                font-weight 200px
                line-height 12px
                color rgba(255,255,255,1)
                display flex
                justify-content space-around
                align-items center
                border-radius 10px
                .count
                    zoom 1
                    position relative
                    left 4px
                .arrow_right
                    zoom 1
        & > .bottom
            box-sizing border-box
            width 100%
            height 28px
            padding 0px 26px 0 12px
            background rgba(7,17,27,.2)
            overflow hidden
            text-overflow ellipsis
            white-space nowrap
            color rgba(255,255,255,1)
            line-height 28px
            font-size 10px
            font-weight 200
            position relative
            .icon
                bg-image(bulletin)
                background-size 100%
                background-repeat no-repeat
                display inline-block
                width 22px
                height 12px
                margin-right 4px
                position relative
                top 1px
            .text
                zoom 1
            .arrow_right
                position absolute
                right 12px
                top 8px
        & > .bg
            position absolute
            left 0
            right  0
            top 0
            bottom  0
            background pink
            z-index -1
            filter blur(10px)
            img
                width 100%
                height 100%
        & > .mask
            position fixed
            left 0
            right  0
            top 0
            bottom  0
            margin auto
            z-index 9
            backdrop-filter blur(10px)
            background rgba(7,17,27,.8)
            overflow auto
            .contentWrap
                @extend .clearfix
                min-height 100%
                .content
                    @extend .clearfix
                    padding-bottom 96px
                    padding-top 64px
                    .title
                        text-align center
                        font-size 16px
                        line-height 16px
                        color rgba(255,255,255,1)
                        font-weight 700
                    .stars
                        background pink
                        height 24px
                        width 100%
                        margin-top 16px
                        margin-bottom 28px
                    .line
                        width 80%
                        margin 0 auto
                    .bulletin
                        width 80%
                        margin 0 auto
                        margin-top 24px
                        box-sizing border-box
                        padding 0 12px
                        color white
                        font-size 12px
                        line-height 24px
            .footer
                margin-top -96px
                width 100%
                height 96px
                line-height 96px
                text-align center
                .close
                    color rgba(255,255,255,.5)
                    font-size 32px
</style>