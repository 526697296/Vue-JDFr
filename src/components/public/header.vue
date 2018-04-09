<template>
<div :class="$style.header">
    <span :class="$style.left">
        <!-- 这里只是做还原，真实的项目中用a或者router-link标签 -->
        <em>注册</em>&nbsp;|&nbsp;<em>登入</em>
    </span>
    <!-- 这里调用btn.vue组件，slot插槽的形式 -->
    <btn :class="$style.btnDwn">APP下载</btn>
</div>
</template>
<script>
// 引入btn.vue组件
import btn from '../core/btn.vue'

export default {
    components:{
        // 注册btn组件
        btn,
    }
}
</script>
<style lang="scss" module>
// module是css模块化,不会造成样式全局污染，感觉和scoped一样
.header{
    color:#666;
    height:1rem /* 100/100 */;
    line-height:1rem /* 100/100 */;
    position:fixed;
    top:0;
    left:0;
    right:0;
    font-size:.32rem /* 32/100 */;
    background: #fff url("//m.jr.jd.com/spe/qyy/main/images/jr-logo.png") center center no-repeat;
    // 小技巧，设置图片的大小，这样的图片就会自适应，还能起到居中的效果
    background-size: auto 50%;
    // 这里因为头部是吸顶效果，所以层级要最高，才能盖住其他的
    z-index: 100;
    .left{
        font-size:.28rem /* 28/100 */;
        height:.3rem /* 30/100 */;
        line-height:.3rem /* 30/100 */;
        margin:.17rem /* 17/100 */ 0 0 .18rem /* 18/100 */;
    }
    .btnDwn{
        float: right;
        font-size:.24rem /* 24/100 */;
        border-width:0;
        height:.56rem /* 56/100 */;
        line-height:.56rem /* 56/100 */;
        min-width:1.2rem /* 120/100 */;
        padding:0;
        border-radius:.04rem /* 4/100 */;
        margin:.28rem /* 28/100 */ .24rem /* 24/100 */ 0 0;
    }
}
</style>
