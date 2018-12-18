<template>
  <div class="alert alert-secondary greeting">
    <h3>Are you ready ?</h3>
    <button @click="finalClick">GO</button>
  </div>
</template>

<script>
  export default {
    name: 'Finish',
    data() {
      return {}
    },
    props: ['finishMessage', 'numberOfSteps', 'success'],
    computed: {
      finalMessage() {
        return this.success == this.numberOfSteps ? 'Good Job! Continue?' : `You failed ${this.success}/${this.numberOfSteps} is correct`
      }
    },
    methods:{
      finalClick(){
        this.$emit('finalClick', this.success == this.numberOfSteps)
      }
    }
  }
</script>

<style scoped>
  .greeting {
    width: 70%;
    margin: 20px auto;
    text-align: center;
  }
</style>
