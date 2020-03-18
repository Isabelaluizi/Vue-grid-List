<template>
    <div id="grid-container" class="grid-style">
    <Tweet v-for="tweet in tweets" :key="tweet.content" :content="tweet.content" :author="tweet.author" />
    </div>
</template>

<script>
import Tweet from './Tweet.vue'

export default {
    name: 'TweetList',
    components: {
        Tweet
    },
    props: {
        tweets: Array
    }, 
    mounted: function() {
        this.$root.$on("changeToList", this.changeCardToList);
        this.$root.$on("changeToCard", this.changeListToCard);
    },
    methods: {
        changeCardToList: function() {
            let change = document.getElementById("grid-container");
            change.classList.remove("grid-style");
        },
        changeListToCard: function() {
            let change = document.getElementById("grid-container");
            change.classList.add("grid-style");
        }
    }  
}
</script>

<style scoped>
.grid-style {
    display: grid;
    grid-template-columns: auto auto auto;
    grid-template-rows: auto auto auto;
    row-gap: 5vh;
    column-gap: 5vw;
    margin-left: 5vw;
    margin-right: 5vw;
}
</style>