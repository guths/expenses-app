<template>
  <div id="app">
    <base-spinner></base-spinner>
    <router-view></router-view>
  </div>
</template>

<script>
import BaseSpinner from './components/BaseSpinner';

export default {
  components: {
    BaseSpinner
  },
  methods: {
    hideSpinner () {
      this.$root.$emit('Spinner::show')
    }
  },
  mounted() {
    console.log(this.$firebase)
  }
}
</script>

<style lang="scss">
  #app{
    min-height: 100vh;
    background-color: var(--dark);
  }
</style>
