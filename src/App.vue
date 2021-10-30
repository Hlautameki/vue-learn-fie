<template>
  <ninja-coffee></ninja-coffee>
</template>

<script>
import Hello from './components/Hello/Hello.vue'
import NinjaCoffee from './components/NinjaCoffee/NinjaCoffee.vue'

export default {
  name: 'App',
  components: {
    Hello,
    NinjaCoffee
  }
}
</script>


<style lang="stylus">
// #app
//   font-family Avenir, Helvetica, Arial, sans-serif
//   -webkit-font-smoothing antialiased
//   -moz-osx-font-smoothing grayscale
//   text-align center
//   color #2c3e50
//   margin-top 60px
</style>
