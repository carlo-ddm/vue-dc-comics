<template>
  <div class="icon-items" >
    <div class="container">
    <ul>
      <li v-for="(icon,index) in icons" :key="`icons_${index}`" >
        <img :src="`${icon.src}`" :alt="icon.iconTitle">
        <span>{{icon.iconTitle}}</span>
      </li>
    </ul>
    </div>
  </div>
</template>

<script>
import one from '../assets/img/buy-comics-digital-comics.png';
import two from '../assets/img/buy-comics-merchandise.png';
import three from '../assets/img/buy-comics-subscriptions.png';
import four from '../assets/img/buy-comics-shop-locator.png';
import five from '../assets/img/buy-dc-power-visa.svg';

export default {
  name: 'IconsItems',
  data(){
    return {
      icons: [
        {
          src: one,
          iconTitle: 'digital comics'
        },
         {
          src: two,
          iconTitle: 'dc merchandis'
        },
         {
          src: three,
          iconTitle: 'subscription'
        },
         {
          src: four,
          iconTitle: 'comic shop locator'
        },
         {
          src: five,
          iconTitle: 'dc power visa'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scope>
// import
@import '../assets/styles/mixines';
@import '../assets/styles/vars';

.icon-items {
  @include d-flex-jc-ac;
  background-color: $colorePrimario;
  height: 110px;
  ul {
    @include d-flex-jc-ac;
    height: 90px;
    li {
      @include d-flex-jc-ac;
      list-style: none;
      margin: 0 30px;
      img {
        width: 40px;
        margin: 10px;
      }
      span {
        text-transform: uppercase;
        font-size: 12px;
      }
    }
  }
}

</style>