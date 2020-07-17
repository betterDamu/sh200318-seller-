<template>
  <div id="app">
    <seller-header></seller-header>
    <div class="navs">
      <div class="nav">
        <router-link to="/goods">goods</router-link>
      </div>
      <div class="nav">
        <router-link to="/ratings">ratings</router-link>
      </div>
      <div class="nav">
        <router-link to="/seller">seller</router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  import {mapState} from "vuex";
  import header from "components/header/header.vue";
  export default {
    name: 'App',
    computed:{
        ...mapState(["test"])
    },
    components:{
        "seller-header":header
    } ,
    async mounted(){
        const seller = await this.$axios.get("/api/seller");
        console.log(seller);
    }
  }
</script>

<style scoped lang="stylus">
  #app
    .navs
      .nav
        a
          color red
</style>
