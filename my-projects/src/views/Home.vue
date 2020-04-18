<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <!-- <Kform :msg="msg" ref="form" @handleClick="handleClick" />
    <kFormItem>
      <template #number>12313215</template>
      <template #files="{bar}">{{bar}}</template>
    </kFormItem> -->

    <Einput></Einput>
  </div>
</template>

<script>
  // @ is an alias to /src  
  // import HelloWorld from "@/components/HelloWorld.vue";
  // import Kform from "@/components/form/Kform";
  // import kFormItem from "@/components/form/KFormItem";
  import Einput from "@/components/froms/Einput"

  export default {
    name: "Home",
    // provide() {
    //   return { dong: "" };
    // },
    components: {
      // HelloWorld,
      Kform,
      kFormItem
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