<template>
  <div v-if="visible" class="base-spinner fa-3x">
    <i class="fas fa-circle-notch fa-spin"></i>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false
    }
  },
  created() {
    this.$root.$on('Spinner::show', this.changeSpinner)

    this.$root.$on('Spinner::hide', this.changeSpinner)
  },
  name: 'base-spinner',
  methods: {
    changeSpinner () {
      this.visible = !this.visible;
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables';

.base-spinner {
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: $dark-medium;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  color: $featured;
}
</style>
