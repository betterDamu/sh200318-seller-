<template>
    <div class="lineWrap">
        <span class="line"></span>
        <slot></slot>
        <span class="line"></span>
    </div>
</template>

<script>
    export default {
        name: "line"
    }
</script>

<style scoped lang="stylus">
    .lineWrap
        color rgba(255,255,255,1)
        display flex
        align-items center
        .line
            height 1px
            background  rgba(255,255,255,1)
            flex 1
            &:nth-child(1)
                margin-right 12px
            &:nth-child(3)
                margin-left 12px

</style>