

<template>
 <h1>hayy there</h1>
 <h3>how fast are u </h3>

 <button @click="start" :disabled="isplaying">play</button>
 <Block v-if="isplaying" :delay="delay" @end="endgame"/>
 <p v-if="showresult">reaction time :{{ score}}</p>
</template>


<script >
import Block from './components/Block.vue'
export default {
  components: {Block},
  data(){
    return{
      isplaying: false,
      delay:null,
      score:null,
      showresult:false
    }
  },
  methods:{
    start(){
      this.delay = 2000+Math.random()*5000
         this.isplaying = true
    },
    endgame(reactiofortime){
        this.score = reactiofortime
        this.isplaying = false
        this.showresult = true
    }
  }
}

</script>
<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
.button{
  background-color: aquamarine;
}
</style>
