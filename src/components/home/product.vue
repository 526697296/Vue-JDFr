<template>
<!-- 调用封装得panel组件 -->
  <Panel title="众筹新品" :class="$style.panel">
      <!-- 设定一个容器 -->
      <section :class="$style.content">
          <!-- 日常开发中>应该用字体图标 -->
          <!-- 真实业务场景中应该用router-link -->
          <div :class="$style.arrow">更多尖货 ></div>
          <!-- 调用封装得slider组件 -->
          <!-- options属性slider自带得，在slider组件中封装好了，这里直接绑定 -->
          <!-- 数据进去就好 -->
          <Slider :options="options" :items="items" cname="product-slider"></Slider>
      </section>
  </Panel>
</template>
<script>
// 引入组件
import Panel from '../core/panel.vue'
import Slider from '../core/slider.vue'
export default{
    // 注册组件
    components:{
        Panel,
        Slider
    },
    data(){
        return{
            items:[{
                href:"home",
                src:"../../../static/img/home/home-zc1.jpg"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-zc2.jpg"
            },
            {
                href:"home",
                src:"../../../static/img/home/home-zc3.jpg"
            }],
            // 设置组件得属性值
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
<style lang="scss">
.product-slider{
    // 这个是我们设置swiper得样式，swiper-container是swiper官方得属性
    .swiper-container{
        // border-box = 元素+内填充+padding
        box-sizing: border-box;
        padding:0 .24rem /* 24/100 */ 0 .24rem /* 24/100 */;
        .swiper-slide{
            a{
                display: inline-block;
                width:100%;
                img{
                    width:100%;  //防止图片过小
                    display: block;
                    height: 3.14rem /* 314/100 */;
                    border:.01rem /* 1/100 */ solid #fafafa;
                }
            }
        }
    }
}
</style>
<style lang="scss" module>
@import '../../../src/assets/css/element.scss';
// 设置该组件得样式
.panel{
    @include panel;
    .content{
        padding-bottom:.4rem /* 40/100 */;
        position: relative;
        &>div{
            position: absolute;
            font-size:.28rem /* 28/100 */;
            color:#999;
            right:.2rem /* 20/100 */;
            top:-.7rem /* 70/100 */;
        }
    }
}

</style>

