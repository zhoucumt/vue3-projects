<template>
  <div class="hello">
    HelloWorld {{count}}
    <div>{{plusOne}}</div>
  </div>
</template>

<script>
import {ref, reactive, computed} from 'vue';
export default {
  name: 'HelloWorld',

  setup() {
    const count = ref(1)
    const plusOne = computed(() => count.value + 1)

    console.log(plusOne.value) // 2
    console.log(count)
    // console.log(plusOne.value++)
    plusOne.value++ // error
    return {
      count,
      plusOne
    }
  },

  props: {
    msg: String
  }
}
</script>

<style scoped lang="less">
</style>
