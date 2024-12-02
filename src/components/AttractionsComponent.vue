<template >
    <div class="img-div">
              <img :src="attraction.image" alt="attraction" class="attraction-image" />
            </div>
            <p class="attraction-name">{{ attraction.name}}</p>
    </template>
    
    
    
    
    
    <script>
    export default{
     name: "AttractionsComponent",
     props:{
        attraction: Object
      },
    };
    </script>
    
    <style>
    .attraction-image{
      width: 200px;
      height: 100px;
    }
    
    </style>