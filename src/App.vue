<template>
  <Header/>
  <FeaturedMovie/>
  <NewArrival/>
  <ExclusiveVideos/>
  <FeaturedCasts/>
  <Footer/>
</template>

<script>
import Header from "./components/Header.vue";
import FeaturedMovie from "./components/FeaturedMovie.vue";
import NewArrival from "./components/NewArrival.vue";
import ExclusiveVideos from "./components/ExclusiveVideos.vue";
import FeaturedCasts from "./components/FeaturedCasts.vue";
import Footer from "./components/Footer.vue";
export default {
  components: {
    Header,
    FeaturedMovie,
    NewArrival,
    ExclusiveVideos,
    FeaturedCasts,
    Footer
  }
}
</script>
