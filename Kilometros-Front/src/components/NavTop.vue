<template>
  <div class="navTop">
    <nav>
      <a href="">GALERY</a>
      <a href="">PROYECTS</a>
      <a href="">LOCATION</a>
      <a href="">NEWS</a>
      <a href="">CONTACT</a>
    </nav>
  </div>
</template>

<script>
  export default {
    name:'NavTop'
  }
</script>

<style lang="scss" scoped>
@import "~sass/utils/index";

  .navTop {
    padding-top: 20px;
    display: flex;
    justify-content: flex-end;
    height: 70px;
    width: 100%;
    @include mobile {
      display: none;
    }
  }

  a {
    font-family: $font;
    color: #fff;
    text-decoration: none;
    letter-spacing: 0.15em;

    display: inline-block;
    padding: 15px 20px;
    position: relative;
  }
  a:after {
    background: none repeat scroll 0 0 transparent;
    bottom: 0;
    content: "";
    display: block;
    height: 2px;
    left: 50%;
    position: absolute;
    background: rgb(28, 151, 253);
    transition: width 0.3s ease 0s, left 0.3s ease 0s;
    width: 0;
  }
  a:hover:after {
    width: 100%;
    left: 0;
  }
</style>
