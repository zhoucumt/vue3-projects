<template>
  <div class="hello">
    HelloWorld
  </div>
</template>

<script>
import {ref, reactive, watchEffect} from 'vue';
export default {
  name: 'HelloWorld',

  setup() {
    const state = reactive({
      name: 'Jack',
      age: 1,
      address: 'aaa'
    });
    watchEffect(() => {
      console.log('123');
    })
  },

  props: {
    msg: String
  }
}
</script>

<style scoped lang="less">
</style>
