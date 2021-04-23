<template>
  <div id="app">
    <base-spinner></base-spinner>
    <button @click="hideSpinner()" class="btn btn-primary">Show Spinner</button>
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
  }
}
</script>

<style lang="scss">

</style>
