<template>
  <div>
    <div @click="handleClick">{{msg}}</div>
    <span @click="$parent.$emit('borather','123456')">{{foo}}</span>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  props: {
    msg: {
      type: String,
      default: "456454566456"
    }
  },
  // inject: ["dong"],
  data() {
    return {
      foo: "value"
    };
  },
  methods: {
    handleClick(e: object) {
      // console.log(this.dong);
      this.$emit("handleClick", "aaaa", e);
    }
  }
});
</script>

<style scoped>
</style>