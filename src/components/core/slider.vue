<template>
    <section :class="cname">
        <!-- 这是一个抽象的轮播图组件的编写，依赖于vue-awesome-swiper，先npm安装
        ,这个组件是抽象的，类名是引入进来的，然后swiper的各个参数都是传递进来的，
        适合各种轮播图效果 -->
        <!-- :options是官方规定的，后面的option是我们自己定义的
        通过props传递参数进来 -->
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <!-- 指示器||v-if="options.pagination"判断有没有指示器，有的不需要 -->
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination">

            </div>
        </swiper>
    </section>
</template>
<script>
//引入vue-awesome-swiper
import { swiper, swiperSlide } from 'vue-awesome-swiper'

export default {
    // 注册swiper,swiperSlide组件
    components:{
        swiper,
        swiperSlide
    },
    props:{
        cname:{
            type:String,
            default:"",
        },
        options:{
            // 类型是一个对象的形式,参数在default里面编写
            type:Object, 
            //不是一个对象，我们需要返回一个对象 
            default(){
                return{
                    autoplay:true,
                    loop:true,
                    pagination:{
                        el:".swiper-pagination",
                        },
                    notNextTick:false
                    }
                }
            },
            //items这个是传递slide里面的内容，传递一个数组进来，可以是图片或者其他的东西
            items:{
                type:Array,
                default(){
                    // []里面也可以自己添加数据,这样可以直接在这里展示效果
                    return []
                }
            }
        }
}
</script>
<style lang="css">
/* 引入vue-awesome-swiper样式 */
/* @import "swiper/dist/css/swiper.css"; */
/* 这里定义的是图片的大小,我自己临时定义的,不然没法转换rem,一个弊端,哎 */

</style>