<template>
  <div>
    <slot name="number"></slot>
    {{msg}}
    <slot name="files" bar="我是作用域传参"></slot>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      msg: "我是兄弟子组件"
    };
  },
  created() {
    this.$parent.$on("borather", (a: string) => {
      console.log(a);
    });
  }
});
</script>

<style scoped>
</style>