<template>
  <div id="app">
    <timeline-view></timeline-view>
  </div>
</template>

<script>
import TimelineView from './TimelineRefect/index'
import '../node_modules/font-awesome/scss/font-awesome.scss'
export default {
  name: 'App',
  components: {
      TimelineView,
    //   AnimationIndex
  }
}
</script>

<style lang="scss" scoped>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
