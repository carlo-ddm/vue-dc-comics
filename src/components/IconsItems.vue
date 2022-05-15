<template>
  <div class="icon-items" >
    <div class="container">
    <ul>
      <li v-for="(icon,index) in icons" :key="`icons_${index}`" >
        <img src="../assets/img/buy-comics-digital-comics.png" :alt="icon.iconTitle">
        <span>{{icon.iconTitle}}</span>
      </li>
    </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IconsItems',
  data(){
    return {
      icons: [
        {
          imag: 'buy-comics-digital-comics.png',
          iconTitle: 'digital comics'
        },
         {
          imag: 'buy-comics-merchandise.png',
          iconTitle: 'dc merchandis'
        },
         {
          imag: 'buy-comics-subscriptions.png',
          iconTitle: 'subscription'
        },
         {
          imag: 'buy-comics-shop-locator.png',
          iconTitle: 'comic shop locator'
        },
         {
          imag: 'buy-dc-power-visa.svg',
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
  background-color: $colorePrimario;
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