<template lang="html">
  <div>
    <Heador></Heador>
    <Hslider></Hslider>
    <Novice></Novice>
    <Product></Product>
    <Yqyc></Yqyc>
    <Advise></Advise>
  </div>
</template>

<script>

import Heador from '../public/header.vue'
import Hslider from './hslider.vue'
import Novice from './novice.vue'
import Yqyc from './yqyc.vue'
import Advise from '../public/advise.vue'
import Product from '../home/product.vue'
export default {
  components:{
    Heador,
    Hslider,
    Novice,
    Yqyc,
    Advise,
    Product
  }
}
</script>

<style lang="scss" module>
  

</style>
