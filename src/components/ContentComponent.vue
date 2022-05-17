<template>
  <div class="content">
    <div class="jumbotron">
    </div>
    <div class="container" >
      <div class="card" v-for="(card,index) in cards" :key="index">
        <img :src="card.thumb" alt="">
        <span>{{card.series}}</span>
      </div>

      <button><strong>load more</strong></button>
      
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
@import '../assets/styles/vars';

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
    justify-content: center;

    .card {
      flex-basis: calc(100% / 6);
      margin: 20px 0;

      span {
        margin: 5px 0;
      }


    }
    
    button {
      padding: 5px 50px;
      margin: 10px 0;
      background-color: $colorePrimario;
      border: none;
      color: white;
      text-transform: uppercase;
      cursor: pointer;
    }

    
  }
}
</style>