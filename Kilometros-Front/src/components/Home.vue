
<template>
    <div class="Home">
      <NavTop />
      <div class="titleWrapper">
        <div class="title">
          KILOMETROS
        </div>
        <div class="subtitle">
          OF EXPERIENCE IN THE INDUSTRY
        </div>
      </div>

      <div class="textWrapper">
        <span class="text">At Construction we strive to excel in every service we provide, adding value for our customers wherever</span>
      </div>

      <div class="buttonWrapper">
        <button class="button is-top" >SEE ALL PROYECTS</button>
        <button class="button" >ABOUT US</button>
      </div>
    </div>
</template>

<script>
  import NavTop from './NavTop';

  export default {
    name: 'Home',
    components: {
      NavTop,
    },

    data () {
      return {
        autoplay: true,
        perPage:1,
        paginationPadding: 8
      }
    }
  }
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

@import "~bulma/sass/utilities/_all";
@import "~sass/utils/index";
@import "~bulma/sass/elements/button";

.Home {
  background-image: url("../assets/banner.jpg");
  background-size: cover;
  background-position: center center;
  height: 590.2px;
  padding: 0 36px;
  @include desktop {
    height: 688px;
  }

}

.titleWrapper {
  align-items: center;
  display: flex;
  padding-top: 87px;
  margin-bottom: 43px;
  flex-direction: column;
  @include mobile {
    padding-top: 150px;
  }
}

.title {
  color: #fff;
  font-family: 'Raleway', sans-serif;
  font-size: 26px;
  margin-bottom: 7px;

    @include tablet {
      font-size: 55px;

    }
}

.subtitle {
  color: #fff;
  font-family: 'Raleway', sans-serif;
  font-size: 14px;
  font-weight: bold;
}

.textWrapper {
  text-align: center;
  margin-bottom: 20px;
  @include tablet {
    margin-bottom: 70px;
  }
}

.text {
  color: #fff;
  display: block;
  font-family: 'Raleway', sans-serif;
  font-size: 18px;
}

.buttonWrapper {
  display: flex;
  flex-direction: column;
  align-items: center;

  @include tablet {
    flex-direction: row;
    justify-content: center;
  }
}

.button {
  color: #fff;
  background: transparent;
  border-style: solid;
  border-color: lightgray;
  border-radius: 27px;
  border-width: 2px;
  width: 70%;
  height: 55px;
  font-family: 'Raleway', sans-serif;

  &.is-top {
    margin-bottom: 10px;

    @include tablet {
      margin-bottom: 0;
      margin-right: 60px;
    }
  }

  @include tablet {
    width: 200px;
  }
}
</style>
