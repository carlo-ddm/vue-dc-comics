<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="dc_logo">
      <ul>
        <li v-for="(item,index) in menu" :key="`menu_${index}`">
          <a href="item.href">
            {{item.name}}
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data(){
    return{
      menu:[
        {
          href: '#',
          name: 'characters',
          active: false
        },
        {
          href: '#',
          name: 'comics',
          active: true
        },
        {
          href: '#',
          name: 'movies',
          active: false
        },
        {
          href: '#',
          name: 'tv',
          active: false
        },
        {
          href: '#',
          name: 'games',
          active: false
        },
        {
          href: '#',
          name: 'collectibles',
          active: false
        },
        {
          href: '#',
          name: 'videos',
          active: false
        },
        {
          href: '#',
          name: 'fans',
          active: false
        },
        {
          href: '#',
          name: 'news',
          active: false
        },
        {
          href: '#',
          name: 'shop',
          active: false
        },
      ]
      
    }
  }
}
</script>

<style lang="scss" scope>
//import
@import '../assets/styles/mixines';
@import '../assets/styles/utilities';

header .container{
  @include d-flex-jc-ac;
  height: 100px;

  img {
    margin: 0 10px;
    width: 70px;
  }

  ul {
    @include d-flex-jc-ac;
    
    li {
      @include d-flex-jc-ac;
      list-style: none;

      a {
        margin: 0 10px;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 12px;
        font-weight: bold;
        color: #363636;
      }
    }

    }
    
}

</style>