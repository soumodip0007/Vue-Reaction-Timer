<template>
  <p>Reaction Time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
   props: ['score'],
   data(){
    return{
      rank: null
    }
   },
   mounted(){
        if(this.score < 350) {
            this.rank = 'You are pro'
        } else if (this.score < 450) {
            this.rank = 'Ok! not bad'
        } else {
            this.rank = 'lol - noob!'
        }
   }
}
</script>

<style>
   .rank {
    font-size: 1.4em;
    color: #007BFF;
    font-weight: bold;
   }
</style>