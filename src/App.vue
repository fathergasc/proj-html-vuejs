<template>
  <div id="app">
    <MyHeader />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
  }
}
</script>

<style lang="scss">

// bootstrap scss
@import '~bootstrap/scss/bootstrap.scss';
// my customs scss
@import './styles/common.scss';
@import './styles/variables.scss';
@import './styles/typography.scss';

</style>
