<template>
  <div :class="[btnClass,cname]">
      <!-- 这里的写法是动态绑定一个类名，然后外界可以在通过props传入一个类名 -->
    <slot></slot>
  </div>
</template>
<script>
export default {
  props:{
    //   定义传入类名的规则，
      cname:{
          type:String,
          default:"",
      }
  },
  data(){
      return{
          btnClass:"btn",
      }
  }
}
</script>
<style lang="scss">
// 引入我们原先封装好的btn样式
@import "../../assets/css/element.scss";

.btn{
    @include btn;
}
</style>
