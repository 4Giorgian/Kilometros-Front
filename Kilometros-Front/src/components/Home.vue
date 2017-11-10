
<template>
    <div class="Home">
      <NavTop />
      <div class="titleWrapper">
        <div class="title">
          {{title}}
        </div>
        <div class="subtitle">
          {{subtitle}}
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
        paginationPadding: 8,
        title: "KILOMETROS",
        subtitle: "OF EXPERIENCE IN THE INDUSTRY",
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
  background-image: url("../assets/tower.jpg");
  background-attachment: fixed;
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
  padding-top: 170px;
  margin-bottom: 43px;
  flex-direction: column;
  @include mobile {
    padding-top: 150px;
  }
}

.title {
  color: #fff;
  font-family: $font;
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
  font-family: $font;
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
  background: rgb(28, 151, 253);
  border-style: solid;
  border-color: rgb(28, 151, 253);
  border-radius: 27px;
  border-width: 2px;
  width: 70%;
  height: 55px;
  font-family: $font;

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
