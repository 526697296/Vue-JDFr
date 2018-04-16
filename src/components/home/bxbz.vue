<template>
  <Panel title="保险保障" :class="$style.panel">
      <section :class="$style.content">
          <Slider :options="options" :items="items" cname="product-slider"></Slider>
      </section>
  </Panel>
</template>
<script>
import Panel from '../core/panel.vue'
import Slider from '../core/slider.vue'
export default{
    components:{
        Panel,
        Slider
    },
    data(){
        return{
            items:[{
                href:"home",
                src:"../../../static/img/home/home-bx1.jpg"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-bx2.jpg"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-bx3.jpg"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-bx4.png"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-bx5.jpg"
            }],
            options:{
                // 设定可视区显示多少页,属性值官方给的
                // https://github.com/surmon-china/vue-awesome-swiper/blob/master/examples/15-freemode.vue
                slidesPerView:2.3,
                spaceBetween: 30,
                // loop:true,
                freeMode: true,
                // pagination: {
                //     el: '.swiper-pagination',
                //     clickable: true
                // }
            }
        }
    }
}
</script>
<style lang="scss" module>
@import '../../../src/assets/css/element.scss';
.panel{
    @include panel;
    // margin-right:0;
    .content{
        padding-bottom:.4rem /* 40/100 */;
        position: relative;
    }
}
</style>

