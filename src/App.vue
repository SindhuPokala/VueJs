<template>
  <div id="app">
    <HeaderComponents />
    <!-- <HomeComponent /> -->
    <BestPlaces :places=places />
    <!-- <LatestBlogs :blogs=blogs /> -->
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue'; 
// import HomeComponent from './components/HomeComponent.vue';
import BestPlaces from './components/BestPlaces.vue';
// import LatestBlogs from './components/Places.vue';

export default {
  name: 'App',
  components: {
    HeaderComponents,
    // HomeComponent,
    BestPlaces,
    // LatestBlogs,
  },
  data(){
    return {
      places: [],
      blogs: []
    }
  },
  methods:{
    async fetchPlaces(){
      const res = await fetch('https://traveltourismnode.onrender.com/api');
      const data = await res.json()
      console.log(data)
      // return data;
      return data.places;
    }
  },
  async created(){
      this.places = await this.fetchPlaces();
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
