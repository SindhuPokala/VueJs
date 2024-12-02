<template class="visiting-places-container">
<h1 class="title">Best Places to Visit</h1>
  <div class="places-container">
    <div v-for="place in places" :key="place.name" class="place-card">
      <SinglePlace :place=place />
    </div>
  </div>
  
   <img class="cover-image" src="@/assets/cover-women.jpg" alt="Travel company logo">
</template>

<script>
import SinglePlace from './SinglePlace.vue';

export default {
  name: 'BestPlaces',
  components:{
    SinglePlace
  },
    props:{
        places: Array
    },
};
</script>

<style scoped>

.visiting-places-container{
display:grid;
justify-items:center;
}

h1{
  color:#009aff;
  margin-top:5%;
}

.places-container {
  margin: 0% 10%;
  /* display: grid; */
  /* gap: 2%; */
  /* grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); */
  /* place-items: center; */
}

.place-card {
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 8px;
  /* text-align: center; */
  display: flex;
  width: 100%;
  gap: 1rem
}
.title{
  text-align: center;
}


</style>
