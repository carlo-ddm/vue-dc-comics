<template>
  <footer>
    <div class="container">
      <div class="up">
        <div class="left">
          <div class="col">
            <h2>dc comics</h2>
            <!-- Prima ul -->
            <ul>
              <li v-for="(link,index) in linksDcComics" :key="`link_${index}`" >
                <a href="">{{link.name}}</a>
              </li>
            </ul>
            <!--  Seconda ul -->
            <h2>shop</h2>
            <ul>
              <li v-for="(link,index) in linksShop" :key="`link_${index}`" >
                <a href="">{{link.name}}</a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>dc</h2>
            <ul>
              <li v-for="(link,index) in linksDc" :key="`link_${index}`" >
                <a href="">{{link.name}}</a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>sites</h2>
            <ul>
              <li v-for="(link,index) in linksSites" :key="`link_${index}`" >
                <a href="">{{link.name}}</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="right">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
      <div class="bottom">
        
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data(){
    return {
      linksDcComics: [
        {
        name: 'caracters',
        href: '#'
      },
      {
        name: 'comics',
        href: '#'
      },
      {
        name: 'movies',
        href: '#'
      },
      {
        name: 'tv',
        href: '#'
      },
      {
        name: 'games',
        href: '#'
      },
      {
        name: 'videos',
        href: '#'
      },
      {
        name: 'news',
        href: '#'
      },
      ],

      linksShop: [
        {
        name: 'shop dc',
        href: '#'
      },
      {
        name: 'shop dC collectibles',
        href: '#'
      },
      ],

      linksDc: [
        {
        name: 'terms of use',
        href: '#'
      },
      {
        name: 'privacy policy (new)',
        href: '#'
      },
      {
        name: 'ad choices',
        href: '#'
      },
      {
        name: 'advertising',
        href: '#'
      },
      {
        name: 'jobs',
        href: '#'
      },
      {
        name: 'subscriptions',
        href: '#'
      },
      {
        name: 'talent workshops',
        href: '#'
      },
      {
        name: 'cPSC certificates',
        href: '#'
      },
      {
        name: 'ratings',
        href: '#'
      },
      {
        name: 'shop help',
        href: '#'
      },
      {
        name: 'contact us',
        href: '#'
      }
      ],

      linksSites: [
        {
          name: 'dC',
          href: '#'
        },
        {
          name: 'mAD magazine',
          href: '#'
        },
        {
          name: 'dC kids',
          href: '#'
        },
        {
          name: 'dC universe',
          href: '#'
        },
        {
          name: 'dC power VISA',
          href: '#'
        }
      ]
    }
  }
};
</script>

<style lang="scss" scope>
//import
@import "../assets/styles/mixines";

footer {
  background-image: url("../assets/img/footer-bg.jpg");
}

h2 {
  margin: 20px 0;
  text-transform: uppercase;
}

.up {
  @include d-flex-jc-ac;
  color: white;
  padding: 0 10px;
  height: 400px;

  .left {
    @include d-flex-jc-ac;
    @include l-r-footer;
    .col {
      width: calc(100% / 3);
      height: 100%;
      ul {
        li {
          list-style: none;
          a{
            @include footer-links;
          }
        }
      }
    }
  }
  .right {
    @include dcImg;
    @include l-r-footer;
    img {
      width: 600px;
    }
  }
}
</style>