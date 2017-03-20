<template>
  <header class="topheader">
    <div class="container">
      <!--<p class="welcome">
        Oh, hi. <strong>Choose something to play</strong>
      </p>-->
      <player></player>
    </div>
  </header>
</template>

<script>
  import Player from './player/Player'
  export default {
    name: 'top-header',
    components: {
      Player
    }
  }
</script>

<style lang='scss'>

  @import '~@/assets/scss/variables';

.topheader {
  width: 100%;
  height: $header-height;
  position: fixed;
  top: 0;
  left: 0;
  padding: $header-padding;
  display: flex;
  align-items: center;
  background-color: #fff;
  z-index: 2;
}

.welcome {
  font-size: 1.1em;
  text-align: center;
}

</style>
