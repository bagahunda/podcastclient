<template>
  <div>
    <transition-group name="fade">
      <podcast-simple :key="podcast.id" v-for="podcast in podcasts" :podcast="podcast"></podcast-simple>
    </transition-group>

    <a href="#" class="load-more" @click.prevent="show">Load older podcasts</a>
  </div>
</template>

<script>
  import { mapActions, mapGetters } from 'vuex'
  import PodcastSimple from './podcasts/Simple'

  export default {
    name: 'home',
    components: {
      PodcastSimple
    },
    computed: {
      ...mapGetters({
        podcasts: 'podcasts/getPodcasts'
      })
    },
    methods: {
      ...mapActions({
        getPodcasts: 'podcasts/getPodcasts'
      })
    },
    mounted () {
      this.getPodcasts()
    }
  }
</script>

<style lang='scss'>

  .load-more {
    display: block;
    padding: 20px;
    margin-bottom: 40px;
    font-weight: 500;
    text-align: center;
    background-color: #fff;
    text-decoration: none;
  }

</style>
