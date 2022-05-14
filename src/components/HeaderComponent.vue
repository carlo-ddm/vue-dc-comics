<template>
  <header>
    <div class="container">
        <div>
        LOGO
        </div>
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
          name: 'characters'
        },
        {
          href: '#',
          name: 'comics'
        },
        {
          href: '#',
          name: 'movies'
        },
        {
          href: '#',
          name: 'tv'
        },
        {
          href: '#',
          name: 'games'
        },
        {
          href: '#',
          name: 'collectibles'
        },
        {
          href: '#',
          name: 'videos'
        },
        {
          href: '#',
          name: 'fans'
        },
        {
          href: '#',
          name: 'news'
        },
        {
          href: '#',
          name: 'shop'
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
  height: 80px;

  ul {
    @include d-flex-jc-ac;
    
    li {
      @include d-flex-jc-ac;
      list-style: none;

      a {
        margin: 10px;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 12px;
        font-weight: bold;
      }
    }

    }
    
}

</style>