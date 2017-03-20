<template>
  <div class="player">
    <div class="player__header">
      <span>Now playing</span>: Podcast Title
    </div>
    <audio class="player__audio" controls autoplay ref="player"></audio>
  </div>
</template>

<script>
  export default {
    name: 'player'
  }
</script>

<style lang="scss">

  .player {
    width: 100%;

    &__header {
      margin-bottom: 20px;
      font-weight: 500;

      span {
        font-weight: 800;
      }
    }

    &__audio {
      width: 100%;
    }
  }

</style>
