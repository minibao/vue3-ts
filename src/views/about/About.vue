<template>
  <div id="teleport-target" style="position: relative;">
    <h3>Tooltips with Vue 3 Teleport</h3>
    <div>
      <modal-button />>
      <teleport to=".container"><span>11111</span></teleport>
    </div>
  </div>
</template>

<script>
import modalButton from './templates/modal-button'

export default {
  components: {
    modalButton
  },
  mounted() {
    window.editorInput = this.test
  },
  methods: {
    addDom() {
      const data = '12dlsfdsflds'
      // const domStr = `<input type="button" value="12333" onclick="javascript:alert(123)" data-attr=${data} />`
      // document.getElementById('list-dom').innerHTML = domStr
      this.$refs['rich-text'].setHtml(`<input type="button" value="12333" onclick="javascript:alert(123)" data-attr=${data} />`)
    },
    test() { // 这里做你想做的东西，不光是方法，其它属性也可以
      console.log(1234)
    }
  }
}
</script>

<style lang="less" scoped>
@import "./styles/about.less";
</style>
