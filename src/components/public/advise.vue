<template>
  <div :class="$style.advise">
      <!-- 帮助中心，在线客服 -->
      <div :class="$style.homehelp" v-for="help in helps" :key="help.img">
          <router-lnik :to="{name : help.href}">
              <img :src="help.img">
          </router-lnik>
      </div>
      <!-- 3个图标==>客户端|触频版|电脑端 -->
      <div :class="$style.list">
          <div :class="$style.item" v-for="item in items" :key="item.img">
              <router-link to="/" tag="div">
                  <img :src="item.img" :alt="item.title">
                  <h4>{{item.title}}</h4>
              </router-link>
          </div>
      </div>

      <ul :class="$style.ullist">
          <li>
              <span>Copyright @ 2004-2018 京东JD.COM版权所有</span>
          </li>
          <li>
              <router-link to="/">
                  <span>投资有风险，购买需谨慎</span>
              </router-link>
         </li>
         <li>
              <router-link to="/">
                  <span>京东金融平台服务协议</span>
              </router-link>
         </li>
         <li>
              <router-link to="/">
                  <span>京东金融隐私政策</span>
              </router-link>
         </li>
      </ul>
  </div>
</template>
<script>
export default {
  name: "advise",
  data() {
    return {
        helps:[{
                href:"home",
                img:"../../../static/img/home/home-help.png"
            }],
        items:[
            {
                img:"../../../static/img/home/home-khd.png",
                title:"客户端"
            },
            {
                img:"../../../static/img/home/home-cpb.png",
                title:"触频版"
            },
            {
                img:"../../../static/img/home/home-dnb.png",
                title:"电脑版"
            },
        ]
    }
  }
};
</script>
<style lang="scss" module>
// @import '../../assets/css/element.scss';

.advise{
    background: #f5f5f5;
    margin-top:0.2rem;
    color:#999;
    .homehelp{
        
        width:100%;
    img{
        width:6.4rem /* 640/100 */;
        height:1.44rem /* 144/100 */;
        }
    }
    .list{
        display: flex;
        padding-top:.4rem /* 40/100 */;
        margin-bottom:.2rem /* 20/100 */;
        flex-direction:row;
        justify-content: space-around;
        .item{
            text-align: center;
            flex:1;
            img{
                height:.9rem /* 90/100 */;
                width:.9rem /* 90/100 */;
            }
            h4{
                font-size: .26rem /* 26/100 */;
                margin-top: .1rem /* 12/100 */;
                color:#999;
            }
        }
    }
    .ullist{
        margin-bottom:.2rem /* 20/100 */;
        font-size:.24rem /* 24/100 */;
        li{
            padding:.26rem /* 12/100 */ .32rem /* 16/100 */;
            border-top: .01rem /* 1/100 */ solid #eee;
            text-align: center;
            span{
                letter-spacing:.01rem;
                display: inline-block;
                font-size:.24rem /* 24/100 */;
                color:#999;
                line-height: .32rem /* 32/100 */;
            }
        }
    }
    
}
</style>
