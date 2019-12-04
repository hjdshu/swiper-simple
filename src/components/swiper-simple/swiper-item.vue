<template>
  <div class="swipe-simple-item">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'swipe-simple-item',
  mounted() {
    this.$parent && this.$parent.swipeItemCreated(this)
  },
  destroyed() {
    this.$parent && this.$parent.swipeItemDestroyed(this)
  }
}
</script>
