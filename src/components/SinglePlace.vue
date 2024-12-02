<template class="latest-blogs-container">
  <div class="img-div">
    <img :src="place.image" :alt="place.name" class="place-image" />
  </div>
  <div class="place-details">
    <h2 class="place-name">{{ place.Destination}}</h2>
      <p class="place-prize">Weather: {{ place.Weather }}</p>
      <p class="place-location">{{ place.Reviews_and_Ratings }}</p>
    <h2>Hotels</h2>
    <div class="hotels">
      <div v-for="hotel in place.Hotels" :key="hotel.name" >
        <HotelsComponent :hotel=hotel />
      </div>
    </div>

    <h2>Attractions</h2>
    <div class="attractions">
      <div v-for="attraction in place.Attractions" :key="attraction.name" >
        <AttractionsComponent :attraction=attraction />
      </div>
    </div>
  </div>

</template>

<script>
import AttractionsComponent from './AttractionsComponent.vue';
import HotelsComponent from './HotelsComponent.vue';

export default {
  name: 'SinglePlace',
  components:{
    HotelsComponent,
    AttractionsComponent
  },
    props:{
      place: Object
    },
};
</script>

<style>
.travel-cover{
height:30%;
width:100%;
}
.travel-cover img{
max-height:100%
}

.place-image {
  width: 100%;
  object-fit: cover;
  border-radius: 8px;
  height: 100%;
}

.place-name {
  font-size: 1.5rem;
  margin: 10px 0;
}

.place-location {
  font-weight: bold;
  color: #555;
}

.place-about {
  color: #666;
}
.place-prize {
  font-weight: bold;
  color: #ff5733; /* Example color */
  margin-top: 10px;
}
.cover-image{
width:100%;
margin-top:10%;
}
.img-div{
  width: 55%
}
.place-details{
  width: 45%;
}
.hotels, .attractions{
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

@media only screen and (max-width: 600px) {
  .place-card{
  flex-direction: column;
  }
  .img-div, .place-details{
    width: 100%;
  }
}

</style>
