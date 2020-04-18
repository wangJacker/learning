<template>
  <div>
    <div @click="handleClick">{{msg}}</div>
    <span>{{foo}}</span>
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
  data() {
    return {
      foo: "value"
    };
  },
  methods: {
    handleClick(e: any) {
      this.$emit("handleClick", "aaaa", e);
    }
  }
});
</script>

<style scoped>
</style>