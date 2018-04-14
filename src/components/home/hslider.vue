<template>
    <div id="hslider">
        <Slider :items="items" :cname="$style.slider">
        <!-- 轮播图部分，调用我们封装好的slider -->
        </Slider>
        <section :class="$style.list">
        <!-- 四个小图标部分 -->
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </div>
</template>
<script>

// 引入slider封装好的组件
import Slider from '../core/slider.vue'

export default {
    name:'hslider',
    // 注册组件
    components:{
        // 注册slider组件
        Slider,
    },
    data(){
        return{
            // 轮播图
            items:[{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t17743/102/1419735038/76755/d0974387/5ac97f30N0b690c0c.jpg?width=750&height=320"
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t18826/81/1450949488/22046/3f694934/5ac9e66aNc7821e16.jpg?width=750&height=320"
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t19162/159/1436094457/37979/2a2c3251/5ac9e6a5Ncb78c9f1.jpg?width=750&height=320"
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t19369/206/1454707890/45803/618b329f/5ac9e7e3Nad569604.jpg?width=750&height=320"
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t19132/326/1430324246/42649/4637640a/5ac9e83eN50f75a37.jpg?width=750&height=320"
            }],
            // 小图标
            enters:[{
                img:"../../../static/img/home/home-yhq.png",
                title:"优惠券",
                href:"home"
            },{
                img:"../../../static/img/home/home-lhb.png",
                title:"领红包",
                href:"home"
            },{
                img:"../../../static/img/home/home-qgb.png",
                title:"抢钢镚",
                href:"home"
            },{
                img:"../../../static/img/home/home-btte.png",
                title:"白条提额",
                href:"home"
            }]
        }
    }
}
</script>
<style lang="scss" module>
// 这个组件是首页home中的轮播图和下面的小图片
//引入公共样式
@import "../../assets/css/element.scss";

.slider{
    margin-top:1.2rem /* 120/100 */;
    img{
    width:6.4rem /* 640/100 */;
    height:2.73rem /* 273/100 */;
}
}
.list{
    @include list(row);
    background:#fff;
    padding-top:.4rem /* 40/100 */;
    padding-bottom: .2rem /* 20/100 */;
    justify-content:space-around;
    a{
        text-decoration: none;
    }
    .item{
        text-align:center;
        img{
           display: inline-block;
           width:.9rem /* 90/100 */;
           height: .9rem /* 90/100 */; 
        }
        h4{
            font-size:.26rem /* 26/100 */;
            margin-top:.12rem /* 12/100 */;
            color:#666;
        }
    }
}
</style>