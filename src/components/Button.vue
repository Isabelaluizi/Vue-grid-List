<template>
<div id="button">
    <h4 v-if="this.button =='List'" id="list-button" @click="changeLayoutList" >List View</h4>
    <h4 v-else id="card-button" @click="changeLayoutCard" >Card View</h4>
</div>
</template>

<script>

export default {
  name: 'Button',
 data: function() {
        return {
            button: "Card"
        }
    },
  methods: {
      changeLayoutList: function() {
          this.button = "Card";
          //console.log(this.button)
          this.$root.$emit('changeToCard')
      },
      changeLayoutCard: function() {
          this.button = "List";
          this.$root.$emit('changeToList')
          //console.log(this.button)
      }
}
}
</script>

<style scoped>
#button {
    border: 1px solid black;
    margin-left:40vw;
    margin-right:40vw;
}
#button:hover {
    background-color: #df6589FF;
 
}
</style>