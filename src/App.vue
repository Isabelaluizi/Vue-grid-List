<template>
  <div id="app">
    <Button />
    <TweetList :tweets="tweets"/>
  </div>
</template>

<script>
import Button from './components/Button.vue'
import TweetList from './components/TweetList.vue'

export default {
  name: 'App',
  components: {
    Button,
    TweetList
  },
  data() {
    return {
      tweets: [{
          content:"Tweet 1",
          author: "Author 1"
        },
        {
          content:"Tweet 2",
          author: "Author 2"
        },
        {
          content:"Tweet 3",
          author: "Author 3"
        },
        {
          content:"Tweet 4",
          author: "Author 4"
        },
        {
          content:"Tweet 5",
          author: "Author 5"
        },
        {
          content:"Tweet 6",
          author: "Author 6"
        },
        {
          content:"Tweet 7",
          author: "Author 7"
        }]
    }
  }
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
</style>
