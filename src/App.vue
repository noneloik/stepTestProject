<template>
  <div class="">
    <div class="progress">
          <div class="progress-bar" role="progressbar" aria-valuenow="70"
          aria-valuemin="0" aria-valuemax="100">
          <span class="sr-only">70% Complete</span>
          </div>
        </div>
    <transition name="rotate" mode="out-in">
    <Start @startGame="switchView" v-if="currentView === 'start'"/>
    <GameCanvas

    v-else-if="currentView === 'gameCanvas'"/>
    <Info

    v-else-if="currentView==='Info'"></Info>
    </transition>
  </div>
</template>

<script>
import Start from './components/start'
import GameCanvas from './components/GameCanvas'
import Info from './components/Info'

export default {
    name: 'App',
    data() {
        return {
          currentView: 'start',
          intMsg:'',
          currentStep:0,
          numberOfSteps:3
        }
    },
    components: {
      Start,

      GameCanvas,
      Info
    },
    computed:{
      currentWith(){
        return this.currentStep/this.numberOfSteps*100
      }
    },
    methods: {
      switchView (view) {
        this.currentView = view
      }
    },
    checkOneAnswer(Msg){
      this.currentStep++
      this.intMsg=Msg
    },
    created() {

    }
}
</script>

<style>
.rotate-enter-active{
       animation: rotateInX 0.3s linear;
    }
    .rotate-leave-active{
        animation: rotateOutX 0.3s linear;
    }
    .rotate-enter, .rotate-leave-to {

}
    @keyframes rotateInX{
        from{transform: rotateX(90deg);}
        to{transform: rotateX(0deg);}
    }
    @keyframes rotateOutX{
        from{transform: rotateX(0deg);}
        to{transform: rotateX(90deg);}
    }

</style>
