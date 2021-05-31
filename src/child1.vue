<template>
  <div class="child-1">
    <p>在子组件当中:</p>
    <p>props-child1Info: {{child1Info}}</p>
    <p>$attrs: {{$attrs}}</p>
    <hr>
    <!-- Child2组件中能直接触发test的原因在于 B组件调用C组件时使用 v-on 绑定了$listeners 属性 -->
    <!-- 通过v-bind 绑定$attrs属性，Child2组件可以直接获取到A组件中传递下来的props（除了child1组件中props声明的）-->
    <Child2 v-on="$listeners" v-bind="$attrs" :mess="mess"></Child2>
  </div>
</template>
<script>
import Child2 from './child2';
export default {
  props: ['child1Info'],
  data() {
    return {
      mess: 'xixi'
    };
  },
  components: { Child2 },
  mounted() {
    this.$emit('test1', '嘻嘻');
  }
};
</script>