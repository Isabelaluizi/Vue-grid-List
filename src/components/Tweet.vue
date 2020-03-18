<template>
    <div class="tweet-container">
        <p>{{ content }}</p>
        <p>{{ author }}</p>
    </div>
</template>

<script>

export default {
    name: 'Tweet',
    props: {
        author: {
            type: String,
            default: "Author Default"
        },
        content: {
            type: String,
            default: "Author Default"
        }
    }  
}
</script>

<style scoped>
.tweet-container {
    padding: 5px;
    margin-top: 5vh;
    background-color:#cbb3cf;
}
</style>