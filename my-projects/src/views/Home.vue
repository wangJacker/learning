<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <Kform :msg="msg" ref="form" @handleClick="handleClick" />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Kform from "@/components/form/Kform";

export default {
  name: "Home",
  components: {
    // HelloWorld,
    Kform
  },
  data() {
    return {
      msg: "我是父组件传下来的值"
    };
  },
  mounted() {
    this.$refs.form.foo;
    console.log((this.$refs.form.foo = "111"));
    console.log((this.$children[0].foo = "455"));
  },
  methods: {
    handleClick(e, a) {
      console.log(e);
      console.log(a);
    }
  }
};
</script>
