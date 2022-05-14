<template>
  <header>
    <div class="container">
        <div>
        LOGO
        </div>
      <ul>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
        <li><a href="#">link</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent'
}
</script>

<style lang="scss" scope>
//import
@import '../assets/styles/mixines';
@import '../assets/styles/utilities';

header .container{
  @include d-flex-jc-ac;

  ul {
    @include d-flex-jc-ac;
    
    li {
      @include d-flex-jc-ac;
      list-style: none;

      a {
        margin: 10px;
        text-decoration: none;
      }
    }

    }
    
}

</style>