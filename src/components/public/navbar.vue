<template>
    <div :class="$style.navbar">
        <router-link tag="div" to="" :class="$style.tabitem">
            <img :src="imgs[0]" alt="首页">
            <p>首页</p>
        </router-link>
        <router-link tag="div" to="" :class="$style.tabitem">
            <img :src="imgs[1]" alt="理财">
            <p>理财</p>
        </router-link>
        <router-link tag="div" to="" :class="$style.tabitem">
            <img :src="imgs[2]" alt="白条">
            <p>白条</p>
        </router-link>
        <router-link tag="div" to="" :class="$style.tabitem">
            <img :src="imgs[3]" alt="我的">
            <p>我的</p>
        </router-link>
    </div>
</template>
<script>
export default {
    data(){
        return{
            imgs:['../../../static/img/nav/nav-sy.png',
                '../../../static/img/nav/nav-lc.png',
                '../../../static/img/nav/nav-bt.png',
                '../../../static/img/nav/nav-wd.png']
        }
    }
}
</script>
<style lang="scss" module>
.navbar{
    display: flex;
    font-size:.22rem /* 22/100 */;
    height:1rem /* 100/100 */;
    // line-height: 1rem /* 100/100 */;
    flex-direction:row;
    position: fixed;
    bottom:0;
    left:0;
    right:0;
    background: #fff;
    z-index:100;
    .tabitem{
        flex:1;
        text-align:center;
        position: relative;
        padding:.1rem /* 14/100 */ 0 0 0;
        img{
            width:.44rem /* 44/100 */; 
            height:.44rem /* 44/100 */;
        }
        p{
           font-size:.22rem /* 22/100 */; 
           color:#656565;
           margin: .06rem /* 6/100 */ 0 0 0;
        }
    }
}

</style>