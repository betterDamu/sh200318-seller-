<template>
  <div id="app">
    <seller-header class="header"></seller-header>
    <div class="navs">
      <div class="nav">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="nav">
        <router-link to="/ratings">评价</router-link>
      </div>
      <div class="nav">
        <router-link to="/seller">商家</router-link>
      </div>
    </div>
    <router-view class="router"></router-view>
  </div>
</template>

<script>
  import {GETSELLER,GETSGOODS,GETRATINGS} from "store/mutation_types.js";
  import {mapActions} from "vuex";
  import header from "components/header/header.vue";
  export default {
    name: 'App',
    methods:{
        ...mapActions([GETSELLER,GETSGOODS,GETRATINGS])
    },
    components:{
        "seller-header":header
    } ,
    async mounted(){
        await this[GETSELLER]();
        await this[GETSGOODS]();
        await this[GETRATINGS]();
    }
  }
</script>

<style scoped lang="stylus">
  @import "./common/stylus/mixin.styl"
  #app
    width 100%
    height 100%
    display flex
    flex-direction column
    .header
      zoom 1
    .navs
      one-px(black)
      display flex
      height 40px
      .nav
        flex 1
        a
          display flex
          justify-content center
          align-items center
          width 100%
          height 100%
          font-size 14px
          color rgba(77,85,93,1)
          &.active
            color rgba(240,20,20,1)

    .router
      flex 1
</style>
