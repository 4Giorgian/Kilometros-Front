<template>
  <div id="app">
    <Home />
    <Gallery />
    <AboutUs />
  </div>
</template>

<script>

import Home from './components/Home';
import AboutUs from './components/AboutUs';
import Gallery from './components/Gallery';

export default {
  name: 'app',
  components: {
    Home,
    AboutUs,
    Gallery,
  }
}
</script>

<style>

</style>
