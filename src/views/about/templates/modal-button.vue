<template>
  <button @click="modalOpen = true">Open full screen modal!</button>
  <teleport to=".container">
    <div v-if="modalOpen" class="modal">
      <div>
        I'm a modal!
        <button @click="modalOpen = false">Close</button>
      </div>
    </div>
  </teleport>
</template>

<script>
export default {
  data() {
    return {
      modalOpen: false
    }
  }
}
</script>
