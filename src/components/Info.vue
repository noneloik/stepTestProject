<template>
  <div class="alert alert-secondary greeting">
    <h3>{{ intMsg }}</h3>
    <button @click="$emit('switchView', 'gameCanvas', true)">Next question</button>
  </div>
</template>

<script>
export default {
  name: 'Info',
  data () {
    return {

    }
  },
  props: ['intMsg']
}
</script>

<style scoped>
.greeting {
    width: 70%;
    margin: 20px auto;
    text-align: center;
}
</style>
