<template>
  <div class="box is-flex is-flex-direction-column is-align-content-center is-align-self-center is-align-items-center">
    <!-- <div style="display:flex; justify-content:center"> -->
    <button class="button is-primary has-background-black">{{buttonContent}}</button>
    <button class="button has-background-warning">{{getButtonContent()}}</button>
    <p><a :href="wykopLink" target="_blank">Wykop</a></p>
  </div>
</template>

<script>
import '../../styl/main.styl'

export default {
  name: 'Hello',
  data() {
    return {
      buttonContent: 'Press Me',
      wykopLink: 'https://www.wykop.pl'
    }
  },
  methods: {
    getButtonContent() {
      return 'Press me'
    }
  }
}
</script>