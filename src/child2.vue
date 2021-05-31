<template>
  <div class="child-2">
    <p>在最里层组件当中child2:</p>
    <p>props-child2Info: {{child2Info}}</p>
    <p> $attrs 的值: {{$attrs}}</p>
    <hr>
  </div>
</template>
<script>
export default {
  props: ['child2Info'],
  data() {
    return {};
  },
  mounted() {
    this.$emit('test2', '哈哈');
  }
};
</script>
