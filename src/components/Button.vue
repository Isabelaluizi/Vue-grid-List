<template>
<div>
    <h4 v-if="this.button =='List'" id="list-button" @click="changeLayoutList" >List View</h4>
    <h4 v-else id="card-button" @click="changeLayoutCard" >Card View</h4>
</div>
</template>

<script>

export default {
  name: 'Button',
 data: function() {
        return {
            button: "List"
        }
    },
  methods: {
      changeLayoutList: function() {
          this.button = "Card";
          console.log(this.button)
      },
      changeLayoutCard: function() {
          this.button = "List";
          console.log(this.button)
      }

    //   generateQuote: function() {
    //     this.$root.$emit('newKanyeQuote')
    //   }
}
}
</script>

<style scoped>

</style>