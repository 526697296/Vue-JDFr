<template lang="html">
  <div>
    <Heador></Heador>
    <Hslider></Hslider>
    <Novice></Novice>
    <Product></Product>
    <Bxbz></Bxbz>
    <Yqyc></Yqyc>
    <Advise></Advise>
    <Navbar></Navbar>
  </div>
</template>

<script>

import Heador from '../public/header.vue'
import Hslider from './hslider.vue'
import Novice from './novice.vue'
import Yqyc from './yqyc.vue'
import Advise from '../public/advise.vue'
import Product from '../home/product.vue'
import Navbar from '../public/navbar.vue'
import Bxbz from '../home/bxbz.vue'
export default {
  components:{
    Heador,
    Hslider,
    Novice,
    Yqyc,
    Advise,
    Product,
    Navbar,
    Bxbz
  }
}
</script>

<style lang="scss" module>
  

</style>
