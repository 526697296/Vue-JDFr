<template>
  <section :class="$style.yqyc">
      <!-- 有钱有车 -->
      <Panel title="有钱有车" :class="$style.panel">
          <section :class="$style.img1">
          <div :class="$style.img11" v-for="yqyc in yqycs" :key="yqyc.img">
              <router-link :to="{name : yqyc.href}">
                  <img :src="yqyc.img">
              </router-link>
          </div>
          </section>
      </Panel>
      <!-- 五个小图标 -->
      <section :class="$style.list">
      <div :class="$style.item" v-for="items in itemss" :key="items.img">
          <!-- 因为点击是可以跳转的，所以要用router-link -->
          <router-link :to="{name: items.href}">
                <img :src="items.img" :alt="items.title">
                <h4>{{items.title}}</h4>
          </router-link>
      </div>
      </section>
      
  </section>
</template>
<script>
import Panel from '../core/panel.vue'
export default{
    name:'yqyc',
    components:{
        Panel,
    },
    data(){
        return{
            yqycs:[
                {
                    href:"home",
                    img:"../../../static/img/home/home-yqycl.png"
                },
                {
                    href:"home",
                    img:"../../../static/img/home/home-yqycr.jpg"
                }
            ],
            itemss:[
                {
                    href:"home",
                    title:"旅游",
                    img:"../../../static/img/home/home-ly.png"
                },
                {
                    href:"home",
                    title:"医美",
                    img:"../../../static/img/home/home-ym.png"
                },
                {
                    href:"home",
                    title:"抵贷",
                    img:"../../../static/img/home/home-fdd.png"
                },
                {
                    href:"home",
                    title:"驾校",
                    img:"../../../static/img/home/home-jx.png"
                },
                {
                    href:"home",
                    title:"分期用",
                    img:"../../../static/img/home/home-fqy.png"
                },
            ]
        }
    }
}
</script>
<style lang="scss" module>
@import "../../assets/css/element.scss";

.panel{
    @include panel;
    margin-bottom:0;
    .img1{
        background: #fff;
        width:100%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        .img11{
            width:50%;
            // padding:.2rem /* 20/100 */;
            img{
                width:3.2rem /* 260/100 */;
                height:2.0rem;
                // margin-top:0.1rem;
            }
        }

    }
}
.list{
    @include list(row);
    background: #fff;
    padding-top:.34rem /* 40/100 */;
    // margin-bottom:.2rem /* 20/100 */;
    justify-content: space-around;
    .item{
        text-align: center;
        img{
            display: inline-block;
            width:.9rem /* 90/100 */;
            height:.9rem /* 90/100 */;
        }
        h4{
            font-size:.26rem /* 26/100 */;
            color:#666;
            margin-top: .12rem /* 12/100 */;
            text-overflow:ellipsis;
            overflow:hidden;
            white-space:normal;
            margin-bottom:.08rem;
        }
    }
    a{
        text-decoration: none;
    }
}

</style>
