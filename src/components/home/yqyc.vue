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
      <!-- 帮助中心，在线客服 -->
      <div :class="$style.homehelp" v-for="help in helps" :key="help.img">
          <router-lnik :to="{name : help.href}">
              <img :src="help.img">
          </router-lnik>
      </div>
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
            helps:[{
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252"
            }],
            yqycs:[
                {
                    href:"home",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t18913/125/1245872730/32248/a8bc4ea2/5ac180b5N008bdabb.png?width=375&height=233"
                },
                {
                    href:"home",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233"
                }
            ],
            itemss:[
                {
                    href:"home",
                    title:"旅游",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90"
                },
                {
                    href:"home",
                    title:"医美",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90"
                },
                {
                    href:"home",
                    title:"抵贷",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88"
                },
                {
                    href:"home",
                    title:"驾校",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90"
                },
                {
                    href:"home",
                    title:"分期用",
                    img:"//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88"
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
.homehelp{
    margin-top:0.2rem;
    width:100%;
    img{
        width:6.4rem /* 640/100 */;
        height:1.44rem /* 144/100 */;
    }
}
</style>
