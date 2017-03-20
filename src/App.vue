<template>
  <div id="app">
   <top-header></top-header>
   <div class="container">
     <home></home>
   </div>
  </div>
</template>

<script>

import TopHeader from './components/TopHeader'
import Home from './components/Home'

export default {
  name: 'app',
  components: {
    TopHeader,
    Home
  }
}
</script>

<style lang='scss'>

  @import '~@/assets/scss/variables';

  html {
    box-sizing: border-box;
  }

  *, *:after, *:before {
    box-sizing: inherit;
  }

  body {
    margin-top: calc(#{$header-height} + (#{$header-padding} * 2));
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    line-height: 1.5;
    color: #2c3e50;
    background-color: #edeff0;
  }

  a {
    color: rgba($blue, 0.9);
    transition: color 0.1s ease-in-out;

    &:hover {
      color: $blue;
    }
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
    flex: 1;
  }

  .fade-enter-active,
  .fade-enter-leave {
    transition: opacity 0.5s ease-in-out;
  }

  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }

</style>
