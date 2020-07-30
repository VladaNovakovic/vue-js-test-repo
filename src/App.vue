<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <TweetForm />
    <Feed v-bind:feed="feed"/>
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <h5 v-bind:subtitle="message" >{{message}}</h5>
  </div>
</template>

<script>
import TweetForm from './components/TweetForm.vue'
import Feed from './components/Feed.vue'

export default {
  name: 'App',
  components: {
    TweetForm,
    Feed,
  },
  data: () => ({
    message: 'You loaded this page on ' + new Date().toLocaleString(),
    feed: [{
      id: 10,
      user: 'pera',
      message: 'Hi there, this is first tweet',
    }, {
      id: 11,
      user: 'pera',
      message: 'Hi there, this is second tweet',
    }, {
      id: 12,
      user: 'mika',
      message: 'this is my first tweet',
    }, {
      id: 13,
      user: 'laza',
      message: 'tweeter sucks',
    }]
  }),
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  h5 {
    font-size: 10px;
  }
</style>
