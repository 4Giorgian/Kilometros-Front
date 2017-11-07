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
    display: flex;
    height: 70px;
    justify-content: center;
    padding-top: 100px;
    width: 100%;
    @include mobile {
      display: none;
    }
  }

  a {
    font-family: 'Raleway', sans-serif;
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
    background: #fff;
    transition: width 0.3s ease 0s, left 0.3s ease 0s;
    width: 0;
  }
  a:hover:after {
    width: 100%;
    left: 0;
  }
</style>
