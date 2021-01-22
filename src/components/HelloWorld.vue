<template>
  <div class="hello">
    HelloWorld
    <div>{{n}}</div>
     <button @click="addN">点击</button>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
  name: 'HelloWorld',

  setup() {
    const n = ref(1);
    function addN() {
      n.value++;
    }
    return {
      n,
      addN
    }
  },

  props: {
    msg: String
  }
}
</script>

<style scoped lang="less">
</style>
