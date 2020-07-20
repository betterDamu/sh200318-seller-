<template>
    <div class="goodsWrap">
        <div class="goods">
            <div class="left"></div>
            <div class="right"></div>
        </div>
        <div class="cart"></div>
    </div>
</template>

<script>
    export default {
        name: "goods"
    }
</script>

<style scoped lang="stylus">
.goodsWrap
    display flex
    flex-direction column
    .goods
        flex 1
        background gray
        display flex
        .left
            width 80px
            background red
        .right
            flex 1
            background green
    .cart
        height 46px
        background pink
</style>