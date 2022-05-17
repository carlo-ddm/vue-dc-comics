<template>
  <div class="content">
    <div class="jumbotron">
    </div>
    <div class="container" >
      <div class="card" v-for="(card,index) in cards" :key="index">
        <img :src="card.thumb" alt="">
      </div>
    </div>
    
  </div>
</template>

<script>
import cards from '../assets/data/cards.js';

export default {
  name: 'ContentComponent',
  data(){
    return {
      cards
    }
  }
}
</script>

<style lang="scss" scope>
.content{
  
  background-color: black;
  color: white;

  .jumbotron {
    width: 100%;
    height: 500px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
  }

  .container {
    display: flex;
    flex-wrap: wrap;

    .card {
      flex-basis: calc(100% / 6);
    }
    
  }
}
</style>