<template>
  <div class="podcast">
    <a href="#" class="podcast__play">
      <img class="podcast__play-button" src="../../assets/img/play.svg" alt="Play">
    </a>
    <div class="podcast__details">
      <div class="podcast__sub">2 Days ago</div>
      <h1 class="podcast__header">
        <a href="#">Lorem ipsum dolor sit.</a>
      </h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Delectus quos aliquam, dolore iure ea in, quae ullam vitae enim dignissimos dolorem, voluptates deleniti eum a quidem assumenda earum nam architecto!
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'podcast-simple',
    props: [
      'podcast'
    ]
  }
</script>

<style lang='scss'>
  @import '~@/assets/scss/variables';

  .podcast {
    display: flex;
    min-height: 240px;
    margin-bottom: 40px;
    background-color: #fff;
    border-radius: $global-raduis;
    box-shadow: 0 5px 10px rgba(#000000, 0.05);
    overflow: hidden;

    &__play {
      width: 15%;
      display: none;
      justify-content: center;
      align-items: center;
      background-color: $blue;
      border-top-left-radius: $global-raduis;
      border-bottom-left-radius: $global-raduis;
      overflow: hidden;
      transition: margin-left 0.18s ease-in-out;

      &--hidden {
        margin-left: -15%;
      }

      &:hover {
        .podcast__play-button {
          transform: scale(3.5) rotate(-10deg);
          opacity: 1;
        }
      }

      @media screen and (min-width: 768px) {
        display: flex;
      }
    }

    &__play-button {
      color: #222222;
      opacity: 0.4;
      width: 60%;
      transition: all 0.18s ease-in-out;
    }

    &__details {
      flex: 1;
      padding: 40px;
    }

    &__sub {
      font-weight: 500;
    }

    &__header {
      font-size: 1.6em;

      a {
        text-decoration: none;
      }
    }
  }

</style>
