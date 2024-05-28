<template>
  <p>reaction time {{ score }}ms</p>
  <p>{{ rank }}</p>
</template>

<script>
export default {
  props:['score'],
  data(){
    return{
      rank:null
    }
  },
  mounted(){
    if (this.score<=700){
      this.rank = 'daimn '
    }else if(this.rank<=1000){
      this.rank = 'not bad'
    }else if(this.rank>2000){
      this.rank = 'slow af get checked your daim finger'
    }
  }
}

</script>

<style>

</style>