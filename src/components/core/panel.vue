<template>
  <section :class="[panelClass,cname]">
      <h4>-{{title}}-</h4>
      <slot></slot>
  </section>
</template>
<script>
export default {
    props:{
        cname:{
            type:String,
            default:"",
        },
        title:{
            type:String,
            default:"",
        }
    },
    data(){
        return{
            panelClass:"panel",
        }
    }
}
</script>
<style lang="scss">
// 引入我们原先封装好的panel样式
@import "../../assets/css/element.scss";

.panel{
    @include panel;
}
</style>