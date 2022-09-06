<template>
  <div id="app">
    <MyHeader />
    <MyMain />
    <MyFooter />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter,
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
//fontawesome
@import '~@fortawesome/fontawesome-free/css/all.css';

</style>
