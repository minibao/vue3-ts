<template>
  <div class="home-child">
    {{count}},{{titleColor}}
  </div>
</template>

<script>
// import { ref, toRefs, reactive } from 'vue'
import { ref } from 'vue'

export default {
  props: ['titleColor'],
  setup() {
    // console.log('props', props)
    // console.log('context', context)
    const count = ref('qqq')
    // const book = reactive({ title: 'Vue 3 Guide' })
    // const { titleColor } = toRefs(props)
    // count.value
    return {
      count
    }
  }
}
</script>
