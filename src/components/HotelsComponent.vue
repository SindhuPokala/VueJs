<template class="home-image">
<div class="img-div">
          <img :src="hotel.image" alt="placename" class="hotel-image" />
        </div>
        <p class="hotel-name">{{ hotel.name}}</p>
</template>





<script>
export default{
 name: "HotelsComponent",
 props:{
      hotel: Object
  },
};
</script>

<style>
.hotel-image{
  width: 200px;
  height: 100px;
}

</style>