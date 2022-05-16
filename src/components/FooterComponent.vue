<template>
  <footer>
    <div class="container">
      <div class="up">
        <div class="left">
          <div class="col">
            <h2>dc comics</h2>
            <!-- Prima ul -->
            <ul>
              <li v-for="(link, index) in linksDcComics" :key="`link_${index}`">
                <a href="">{{ link.name }}</a>
              </li>
            </ul>
            <!--  Seconda ul -->
            <h2>shop</h2>
            <ul>
              <li v-for="(link, index) in linksShop" :key="`link_${index}`">
                <a href="">{{ link.name }}</a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>dc</h2>
            <ul>
              <li v-for="(link, index) in linksDc" :key="`link_${index}`">
                <a href="">{{ link.name }}</a>
              </li>
            </ul>
          </div>

          <div class="col">
            <h2>sites</h2>
            <ul>
              <li v-for="(link, index) in linksSites" :key="`link_${index}`">
                <a href="">{{ link.name }}</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="right">
          <img src="../assets/img/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>

    <div class="bottom">
      <div class="container">
        <div class="col left">
          <button>Sign up now</button>
        </div>
        <div class="col right">
          <div class="div">
            <span>follow us</span>
            <ul>
              <li v-for="(social,index) in socials" :key="`socials_${index}`" >
                <img :src="`${social.src}`" alt="social.name" />
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import one from '../assets/img/footer-facebook.png';
import two from '../assets/img/footer-twitter.png';
import three from '../assets/img/footer-twitter.png';
import four from '../assets/img/footer-pinterest.png';
import five from '../assets/img/footer-periscope.png';

export default {
  name: "FooterComponent",
  data() {
    return {
      linksDcComics: [
        {
          name: "caracters",
          href: "#",
        },
        {
          name: "comics",
          href: "#",
        },
        {
          name: "movies",
          href: "#",
        },
        {
          name: "tv",
          href: "#",
        },
        {
          name: "games",
          href: "#",
        },
        {
          name: "videos",
          href: "#",
        },
        {
          name: "news",
          href: "#",
        },
      ],

      linksShop: [
        {
          name: "shop dc",
          href: "#",
        },
        {
          name: "shop dC collectibles",
          href: "#",
        },
      ],

      linksDc: [
        {
          name: "terms of use",
          href: "#",
        },
        {
          name: "privacy policy (new)",
          href: "#",
        },
        {
          name: "ad choices",
          href: "#",
        },
        {
          name: "advertising",
          href: "#",
        },
        {
          name: "jobs",
          href: "#",
        },
        {
          name: "subscriptions",
          href: "#",
        },
        {
          name: "talent workshops",
          href: "#",
        },
        {
          name: "cPSC certificates",
          href: "#",
        },
        {
          name: "ratings",
          href: "#",
        },
        {
          name: "shop help",
          href: "#",
        },
        {
          name: "contact us",
          href: "#",
        },
      ],

      linksSites: [
        {
          name: "dC",
          href: "#",
        },
        {
          name: "mAD magazine",
          href: "#",
        },
        {
          name: "dC kids",
          href: "#",
        },
        {
          name: "dC universe",
          href: "#",
        },
        {
          name: "dC power VISA",
          href: "#",
        },
      ],

      socials:[
        {
          name: 'facebook',
          src: one,
        },
         {
          name: 'twitter',
          src: two,
        },
         {
          name: 'youtube',
          src: three,
        },
         {
          name: 'pinterest',
          src: four,
        },
         {
          name: 'periscope',
          src: five,
        },
      ],
    };
  },
};
</script>


<style lang="scss" scope>
//import
@import "../assets/styles/mixines";

footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-position: center;
  background-size: cover;
}

h2 {
  margin: 20px 0;
  text-transform: uppercase;
}

.up {
  @include d-flex-jc-ac;
  color: white;
  padding: 0 10px;
  height: 49vh;

  .left {
    @include d-flex-jc-ac;
    @include l-r-footer;
    .col {
      width: calc(100% / 3);
      height: 40vh;
      ul {
        li {
          list-style: none;
          a {
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

.bottom {
  @include d-flex-jc-ac;
  width: 100%;
  height: 12vh;
  background-color: #242424;
  .container {
    @include d-flex-jc-ac;
    height: 100%;
    div {
      @include d-flex-jc-ac;
      ul {
        @include d-flex-jc-ac;
        li {
          margin: 10px;
          list-style: none;
        }
      }
    }
  }

  .col.left {
    button {
      border: 2px solid $colorePrimario;
      padding: 15px 20px;
      text-transform: uppercase;
      background-color: #242424;
      color: white;
      cursor: pointer;
    }
  }

  .col.right {
    @include d-flex-jc-ac;
    div {
      span {
        margin: 0 10px;
        font-size: 30px;
        text-transform: capitalize;
        color: $colorePrimario;
      }
    }
  }
}
</style>