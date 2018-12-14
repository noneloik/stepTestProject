<template>
  <div class="">
    <div class="progress">
<<<<<<< HEAD
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
=======
      <div
        class="progress-bar"
        role="progressbar"
        aria-valuenow="70"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{width: currentWidth}"
        >
      <span class="sr-only">70% Complete</span>
      </div>
    </div>
    <transition name="rotate" mode="out-in">
        <Start @startGame="switchView" v-if="currentView === 'start'"/>
        <GameCanvas
            @switchView="switchView"
            @checkOneAnswer="checkOneAnswer"
            v-else-if="currentView === 'gameCanvas'"/>
        <Info
            :intMessage="intMessage"
            v-else-if="currentView === 'Info'"/>
>>>>>>> upstream/master
    </transition>
  </div>
</template>

<script>
import Start from './components/start'
import Info from './components/Info'
import GameCanvas from './components/GameCanvas'
import Info from './components/Info'

export default {
    name: 'App',
    data() {
        return {
          currentView: 'start',
<<<<<<< HEAD
          intMsg:'',
          currentStep:0,
          numberOfSteps:3
=======
          intMessage: '',
          currentStep: 0,
          numberOfSteps: 3
>>>>>>> upstream/master
        }
    },
    components: {
      Start,
<<<<<<< HEAD

      GameCanvas,
      Info
    },
    computed:{
      currentWith(){
        return this.currentStep/this.numberOfSteps*100
=======
      GameCanvas,
      Info
    },
    computed: {
      currentWidth () {
        return (this.currentStep/this.numberOfSteps)*100 + '%';
>>>>>>> upstream/master
      }
    },
    methods: {
      switchView (view) {
        this.currentView = view
      },
      checkOneAnswer (message) {
        this.currentStep++
        console.log(this.currentStep)
        this.intMessage = message
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
<<<<<<< HEAD
.rotate-enter-active{
=======
    .rotate-enter-active{
>>>>>>> upstream/master
       animation: rotateInX 0.3s linear;
    }
    .rotate-leave-active{
        animation: rotateOutX 0.3s linear;
    }
    .rotate-enter, .rotate-leave-to {
<<<<<<< HEAD

}
    @keyframes rotateInX{
        from{transform: rotateX(90deg);}
        to{transform: rotateX(0deg);}
    }
    @keyframes rotateOutX{
        from{transform: rotateX(0deg);}
        to{transform: rotateX(90deg);}
    }
=======
>>>>>>> upstream/master

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
