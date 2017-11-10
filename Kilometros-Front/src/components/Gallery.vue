<template>
  <div class="container">
    <div class="titleWrapper">
      <div class="title">
        {{title}}
      </div>
    </div>
    <button class="button" v-on:click="show('all')">All</button>
    <button class="button" v-on:click="show('business')">Business</button>
    <button class="button" v-on:click="show('entertainment')">Entertainment</button>
    <button class="button" v-on:click="show('interior')">Interior</button>
    <button class="button" v-on:click="show('office')">Office</button>

    <div v-for="img in images" v-if="filter === 'all' || img.types.includes(filter)">

      <img  :src="img.src"/>
      <div v-text="img.name" />
    </div>
  </div>
</template>

<script>

  import gallery1 from '../assets/gallery1.jpg';
  import gallery2 from '../assets/gallery2.jpg';
  import gallery3 from '../assets/gallery3.jpg';
  import gallery4 from '../assets/gallery4.jpg';

  export default {
    name: 'Gallery',
    data () {
      return {
        title: "GALLERY",
        images: [
          { src: gallery1, types:['interior','office'], city:"newYork", name:"Mini Hotel" },
          { src: gallery2, types:['business','office'], city:"newYork", name:"Mini Hotel"},
          { src: gallery3, types:['entertainment','interior'], city:"newYork", name:"Mini Hotel" },
          { src: gallery4, types:['business','office'], city:"newYork", name:"Mini Hotel" },
        ],
        filter: 'all',
      }
    },

    methods: {
      show(type) {
        this.filter = type;
      },

    }
  }
</script>

<style lang="scss">

@import "~bulma/sass/utilities/_all";
@import "~sass/utils/index";
@import "~bulma/sass/elements/button";

.container {
  height: 400px;
  background: black;
}

.title {
  color: white;
}
</style>
