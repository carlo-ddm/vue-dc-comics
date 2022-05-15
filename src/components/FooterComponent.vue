<template>
  <footer>
    <div class="container">
      <div class="up">
        <div class="left">
          <div class="col">
            <h2>dc comics</h2>
            <!-- Prima ul -->
            <ul>
              <li v-for="(link,index) in links" :key="`link_${index}`" >
                <a href="">{{link.name}}</a>
              </li>
            </ul>
            <!--  Seconda ul -->
            <h2>Title 2</h2>
            <ul>
              <li>
                <a href=""></a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>Title</h2>
            <ul>
              <li>
                <a href=""></a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>Title</h2>
            <ul>
              <li>
                <a href=""></a>
              </li>
            </ul>
          </div>
        </div>

        <div class="right">DX</div>
      </div>
      <div class="bottom"></div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data(){
    return {
      links: [
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
        name: 'news',
        href: '#'
      },
      {
        name: 'caracters',
        href: '#'
      },
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
  color: white; //rimuovi
  padding: 10px;
  border: 1px solid black;
  height: 400px;

  .left {
    @include d-flex-jc-ac;
    @include l-r-footer;
    .col {
      width: calc(100% / 3);
      height: 100%;
      border: 2px solid white;
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
    @include l-r-footer;
  }
}
</style>