<template>
  <div id="app">
    <div class="header-outer"  id="sticky">
      <header>
        <h1 class="site-title"><router-link to="/">Tomoro's portfolio</router-link></h1>
      </header>
      <hnav></hnav>
    </div>

    <div class="">
      <transition name="fade">
        <router-view :data="myData"></router-view>
      </transition>
    </div>

    <fnav></fnav>
  </div>
</template>

<script>
import HeaderNav from '@/components/parts/NavHeader'
import FooterNav from '@/components/parts/NavFooter'
export default {
  name: 'app',
  components:{
    hnav:HeaderNav,
    fnav:FooterNav
  }
}
</script>

<style>

/* .header-outer {
  position: fixed;
  width:100%;
  height: 80px;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9999;
  background: #DEF9F2;
}

.site-title{
    float: left;
    width: 30%;
    margin-top: 20px;
    margin-bottom: 15px;
    margin-bottom: 0;
    margin-left: 20px;
    font-size: 2.0rem;
    color:#000644;
  } */


</style>
