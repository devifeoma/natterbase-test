<template>
  <div>
    <app-navbar></app-navbar>
    <app-searchBar></app-searchBar>
    <app-slider></app-slider>
    <app-popular-category></app-popular-category>
    <app-new-stuff></app-new-stuff>
    <app-footer></app-footer>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import SearchBar from "./components/SearchBar.vue";
import Slider from "./components/Slider.vue";
import PopularCategory from "./components/PopularCategory.vue";
import NewStuff from "./components/NewStuff.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    appNavbar: Navbar,
    appSearchBar: SearchBar,
    appSlider: Slider,
    appPopularCategory: PopularCategory,
    appNewStuff: NewStuff,
    appFooter: Footer
  }
};
</script>

<style>
</style>
