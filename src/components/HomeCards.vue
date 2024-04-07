<script setup lang="ts">
const homeCards: NodeListOf<Element> = document.querySelectorAll('.homeCard');
const numberOfCards = 7;
homeCards.forEach((card: Element) => {
    card.addEventListener('mouseenter', () => {
        homeCards.forEach((otherCard: Element) => {
            if (otherCard !== card) {
                (otherCard as HTMLElement).style.transform = 'scale(0.8)';
            }
        });
    });

    card.addEventListener('mouseleave', () => {
        homeCards.forEach((otherCard: Element) => {
            (otherCard as HTMLElement).style.transform = 'scale(1)';
        });
    });
});
</script>

<template>
    <div class="columns">
        <RouterLink to="postone">
            <div class="homeCard">
                <div class="imageSection">        
                </div>
                <div><h2 class="title1">Educating a</h2><h1 class="title2">machine</h1></div>
            </div>
       </RouterLink>

    <!-- this is a placeholder card component amount displayed can be controlled by the number of cards component -->
        <div  v-for="index in numberOfCards" :key="index"  class="homeCard">
            <div class="imageSectionNotAvailable">
                <h1 class="unavailbleBackground">//////////</h1> 
            <h1 class="unavailbleText"> [UNAVAILABLE]</h1>
   
        </div>
            <div><h2 class="commingSoon">Comming soon ...</h2></div>
        </div>
    </div>


<svg style="display: none;">
  <defs>
    <filter id="noise">
      <feTurbulence
        baseFrequency="0.7,0.8"
        seed="0"
        type="fractalNoise"
        result="static"
      >
      <animate
          attributeName="seed"
          values="0;100"
          dur="800ms"
          repeatCount="indefinite" 
 
        />
      </feTurbulence>
      <feDisplacementMap in="SourceGraphic" in2="static" scale="0">
        <animate
          attributeName="scale"
          values="0;20;30;40"
          dur="110ms"
          repeatCount="indefinite" 
                                            
        />
      </feDisplacementMap>
    </filter>  
  </defs>
</svg>

</template>

  
<style scoped>
.title1{
  text-align: start;
  padding: 1px;
    margin-left:10px;
  font-size: 4vh;
  color: black
}
.title2{
    text-align: center;
    font-size: 6vh;
    bottom: 2vh;
    margin-right: 1px;
    position: relative;
    color: black
}
.columns{
    columns: 2;
    text-align: center;
    padding: 1%;
}
.columns:hover .homeCard{
transform: scale(0.8);
}
.columns .homeCard:hover{
transform: scale(1.2);
}
.unavailbleText{
    font-size: 35px;
    color: rgb(0, 0, 0);
    position: relative;
    bottom: 150%;
}
.unavailbleBackground{
    font-size: 250px;
    color: rgb(211, 211, 211);
    position: relative;
    bottom: 40%;
}

.homeCard {
    position: relative;
    border-radius: 5px;
    background-color: rgb(226, 224, 224);
    width: 40vh;
    height: 40vh;
    margin-left: auto;
    margin-right: auto;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
}
.imageSectionNotAvailable {
    position: relative;
    filter: url(#noise);
    border-radius: 5px;
    text-align: center;
    width: 35vh;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
}

.imageSection {
    position: relative;
    background: url("../assets/images/machineLearning.jpg") no-repeat center;
    border-radius: 5px;
    background-size: cover;
    text-align: center;
    width: 26.5vw;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
}

.commingSoon{
   width: 90vh;
    font-size:60px;
    animation: moveBackAndForth 20s ease-in-out infinite;
}

@keyframes moveBackAndForth {
    0%, 100% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(-20%); /* Adjust the value for the desired movement distance */
  }
}

.homeCard:hover {
    transform: scale(1.2); /* Scale up on hover */
}

/* Add transition for scaling back to the original size when hover is removed */
.homeCard:not(:hover) {
    transform: scale(1);
}
@media (min-width: 1024px) {
    .unavailbleText{
    font-size: 35px;
    color: rgb(0, 0, 0);
    position: relative;
    bottom: 150%;
}
.unavailbleBackground{
    font-size: 250px;
    color: rgb(211, 211, 211);
    position: relative;
    bottom: 40%;
}

.homeCard {
    position: relative;
    border-radius: 5px;
    background-color: rgb(226, 224, 224);
    box-shadow: 5px 5px 5px rgb(71, 71, 71, 0.2);
    width: 35vh;
    height: 35vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
}
.imageSectionNotAvailable {
    position: relative;
    filter: url(#noise);
    border-radius: 5px;
    text-align: center;
    width: 35vh;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
}


.image{
    align-content: center;
    width: 100%;
    height: 110%;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}
.imageSection {
    position: relative;
    border-radius: 5px;
    text-align: center;
    width: 35vh;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
}

.commingSoon{
   width: 90vh;
    font-size:60px;
    animation: moveBackAndForth 20s ease-in-out infinite;
}
   .columns{
    text-align: center;
    columns: 3;
    padding: 1%;   
}
}
@media (max-width: 700px) {   
    
    .imageSection {
    position: relative;
    border-radius: 5px;
    text-align: center;
    width: 74vw;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
}
    
    .columns{
    columns: 1;
    padding: 1%;
}}
</style>
