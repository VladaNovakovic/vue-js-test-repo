<template>
  <div class="vue-c-tweet">
    <h4 class="vue-c-tweet__user">{{tweet.user}}</h4>
    <p class="vue-c-tweet__text">{{tweet.message}}</p>
  </div>
</template>

<script>
    export default {
        name: 'Tweet',
        props: {
            tweet: Object,
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .vue-c-tweet {
    padding-top: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid #3eaf7c;
  }

  .vue-c-tweet:nth-child(2n) {
    background-color: #3eaf7c;
  }

  .vue-c-tweet__user {
    margin: 0;
  }

  .vue-c-tweet__text {
    margin: 0;
  }
</style>
