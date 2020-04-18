<template>
  <div class>
    <input type="text" :value="value" @input="handleInput" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  props: {
    value: {
      type: String,
      default: ""
    }
  },
  methods: {
    handleInput(e: any) {
      this.$emit("input", e.target.value);
    }
  }
});
</script>

<style scoped>
</style>