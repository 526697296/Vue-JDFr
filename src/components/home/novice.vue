<template>
  <Panel title="理财精选" :class="$style.panel">
      <!-- 本组件这样写不行，数据应是动态绑定，不能这样写死，通过data返回 -->
      <section :class="$style.content">
          <div :class="$style.div1" style="border-bottom:.01rem /* 1/100 */ solid #eee;">
                <div :class="$style.item">
                    <h5>定期理财<span>90天可质押</span></h5>
                    <p :class="$style.p1">5.50%</p>
                    <p :class="$style.p2">历史年华结算利率</p>
                </div>
                <div :class="$style.item">
                    <h5>年年赢<span>理财推荐</span></h5>
                    <p :class="$style.p1">5.80%</p>
                    <p :class="$style.p2">综合年化收益率</p>
                </div>
          </div>
          <div :class="$style.div1">
              <div :class="$style.item">
                    <h5>机智账户<span>组合投资</span></h5>
                    <p :class="$style.p1">8%-10%</p>
                    <p :class="$style.p2">止盈年华收益率</p>
              </div>
              <div :class="$style.item">
                    <h5>小白基金<span>超短期</span></h5>
                    <p :class="$style.p1">5.00%</p>
                    <p :class="$style.p2">7日年化收益率</p>
              </div>
          </div>
      </section>
  </Panel>
</template>
<script>

import Panel from '../core/panel.vue'
export default{
    components:{
        Panel
    }
}
</script>
<style lang="scss" module>
@import "../../assets/css/element.scss";
.panel{
    @include panel;
    >h4{
        border-bottom: .01rem /* 1/100 */ solid #eee;
    }
    .content{
        .div1{
            width:100%;
            display: flex;
            flex-direction: row;
            .item{
                width:50%;
                flex-grow: 1;
                height:2.18rem /* 218/100 */;
                padding-left: .32rem /* 32/100 */;
                >h5{
                    font-size:.3rem /* 30/100 */;
                    font-weight: 700;
                    color:#666;
                    line-height: .42rem /* 42/100 */;
                    height: .42rem /* 42/100 */;
                    margin:.35rem /* 17/100 */ 0 .10rem /* 8/100 */;
                    span{
                        border:.01rem /* 1/100 */ solid #ff5155;
                        color:#ff5155;
                        line-height: .34rem /* 34/100 */;
                        font-size:.24rem /* 20/100 */;
                        margin-left:.1rem /* 10/100 */;
                    }
                }
                .p1{
                    color:#ff5155;
                    font-weight: 700;
                    font-size:.44rem /* 44/100 */;
                    height:.58rem /* 58/100 */;
                    line-height: .58rem /* 58/100 */;
                    white-space: nowrap;
                    overflow: hidden;
                    text-overflow: ellipsis;
                }
                .p2{
                    font-size:.24rem /* 24/100 */;
                    color:#999;
                    height:.34rem /* 34/100 */;
                    line-height: .34rem /* 34/100 */;
                    white-space: nowrap;
                    overflow: hidden;
                    text-overflow: ellipsis;
                }
            }
        }
       
    }
}

</style>
