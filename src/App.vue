<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header/Header'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
}
</style>
