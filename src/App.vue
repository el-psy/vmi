<template>
  <div id="app">
    <mi-header></mi-header>
    <ad></ad>
    <div class="main-content clearfix">
      <div class="container">
        <sangou></sangou>
        <shouji></shouji>
        <jiadian></jiadian>
        <zhineng></zhineng>
        <dapei></dapei>
        <peijian></peijian>
        <zhoubian></zhoubian>
      </div>
    </div>
    <foot-er></foot-er>
  </div>
</template>



<script>
import MiHeader from './components/Header.vue'
import Ad from './components/ad.vue'
import Sangou from './components/sangou.vue'
import Shouji from './components/shouji.vue'
import Jiadian from './components/jiadian.vue'
import Footer from './components/footer.vue'
import Zhineng from './components/zhineng.vue'
import Dapei from './components/dapei.vue'
import Peijian from './components/peijian.vue'
import Zhoubian from './components/zhoubian.vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    'mi-header': MiHeader,
    'ad':Ad,
    'sangou':Sangou,
    'shouji':Shouji,
    'jiadian':Jiadian,
    'zhineng':Zhineng,
    'dapei':Dapei,
    'peijian':Peijian,
    'zhoubian':Zhoubian,
    'foot-er':Footer
  }
}
</script>

<style lang="less" scoped>
  .main-content {
    padding-top: 4px;
    padding-bottom: 12px;
    background: #f5f5f5;
    .container {
      width: 1226px;
      margin-right: auto;
      margin-left: auto;
      background: #f5f5f5;
    }
  }
</style>