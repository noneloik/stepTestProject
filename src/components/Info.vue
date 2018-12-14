<template>
  <div class="alert alert-secondary greeting">
<<<<<<< HEAD
    <h3>Next quetion?</h3>
    <!-- <button @click="$emit('startGame', 'gameCanvas')">Get Started</button> -->
=======
    <h3>{{ intMessage }}</h3>
    <button >Next question</button>
>>>>>>> upstream/master
  </div>
</template>

<script>
export default {
  name: 'Info',
  data () {
    return {

    }
<<<<<<< HEAD
  }
}
</script>a
=======
  },
  props: ['intMessage']
}
</script>
>>>>>>> upstream/master

<style scoped>
.greeting {
    width: 70%;
    margin: 20px auto;
    text-align: center;
}
</style>
