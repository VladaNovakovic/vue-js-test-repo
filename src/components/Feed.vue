<template>
  <div class="feed">
    <div v-if="feed.length > 0">
      <h3>See what others think</h3>
      <Tweet v-for="tweet in feed" v-bind:key="tweet.id" v-bind:tweet="tweet" />
    </div>
    <h3 v-if="feed.length < 0">There are no new tweets</h3>
  </div>
</template>

<script>
import Tweet from './Tweet.vue'
export default {
    name: 'Feed',
    components: {
        Tweet,
    },
    props: {
        feed: Array,
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    color: #3eaf7c;
  }
</style>
