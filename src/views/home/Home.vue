<template>
  <div class="home">
    <a-button type="primary" @click="increment">{{ count }}, double is {{ double }}</a-button>
    <Child :titleColor="count" data-attr="123333" />
  </div>
</template>

<script>
import { ref, computed, onMounted } from 'vue'
import Child from './templates/home-child'

export default {
  components: {
    Child
  },
  setup() {
    const count = ref(0)
    const titleColor = 'red'
    const double = computed(() => count.value * 2)
    const increment = () => count.value++

    onMounted(() => console.log('component mounted!'))

    return {
      count,
      titleColor,
      double,
      increment
    }
  }
}
</script>

<style lang="less" scoped>
@import "./styles/home.less";
</style>
