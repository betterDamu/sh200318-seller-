<template>
    <ul class="list">
        <li>
            <seller-icon class="icon" size="2" type="discount"></seller-icon>
            <span>在线支付满28减5,满50送邱海峰</span>
        </li>
        <li>
            <seller-icon size="2" type="decrease"></seller-icon>
            <span>单人精彩赛</span>
        </li>
        <li>
            <seller-icon size="2" type="guarantee"></seller-icon>
            <span>海狗人参丸8折抢购</span>
        </li>
        <li>
            <seller-icon size="2" type="invoice"></seller-icon>
            <span>特价影评8折抢购</span>
        </li>
        <li>
            <seller-icon size="2" type="special"></seller-icon>
            <span>单人特色套餐</span>
        </li>
    </ul>
</template>

<script>
    export default {
        name: "list"
    }
</script>

<style scoped lang="stylus">
    .list
        width 80%
        margin 0 auto
        box-sizing border-box
        padding 0 12px
        font-size 12px
        font-weight 200px
        color white
        margin-top 24px
        margin-bottom 28px
        & > li
            display flex
            align-items center
            margin-bottom 12px
            &:last-child
                margin-bottom 0
            .icon
                margin-right 6px

</style>