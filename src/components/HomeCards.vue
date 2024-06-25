<script setup lang="ts">
const homeCards: NodeListOf<Element> = document.querySelectorAll('.homeCard');
const numberOfCards = 7;
</script>

<template>
  <div class="columns">
        <div class="homeCard">
            <div class="imageSection"/>        
            <div class="titleSection">
             <h2 class="title1">
                 Educating a
             </h2>
             <h1 class="title2">
                 machine
             </h1>
             <h3 class="titleDescription">
                 Computers are complex and intricate machines, the biggest marvel of engineering in our lifetime.
                 But how exactly do we use them to solve real world problems? In this post I explain to you how computers are taught to accomplish
                 said tasks.
             </h3>
             <RouterLink class="postOneButton" to="postone">
               Read ->
             </RouterLink>
            </div>
        </div>
    <!-- this is a placeholder card component amount displayed can be controlled by the number of cards component -->
        <div  v-for="index in numberOfCards" :key="index"  class="homeCard">
           <div>
             <h2 class="commingSoon">
               Coming soon ...
             </h2>
           </div>
        </div>
  </div>


<svg>
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

.titleSection {
     width:auto;
     height:70vh;
     padding:10%;
}

.title1 {
     text-align: left;
     padding: 10px;
     font-size: 4vh;
     color: black
}

.title2 {
    text-align: center;
    font-size: 6vh;
    bottom: 2vh;
    margin-bottom: 10%;
    margin-right: 1px;
    position: relative;
    color: black
}

.titleDescription {
   text-align: left;
}

 .postOneButton {
    padding: 5% 15%;
    position: relative;
    top: 10vh;
    font-size: 2vh;
    background-color: white;
    border-radius: 10px;
 } 
.columns {
    top:10vh;
    left: 15vw;
    column-count: 1;
    text-align: center;
    width: auto;
    padding: 1%;
}

.unavailbleText {
    font-size: 30vw;
    color: rgb(0, 0, 0);
    position: relative;
    bottom: 15%;
}

.unavailbleBackground {
    font-size: 250px;
    color: rgb(211, 211, 211);
    position: relative;
    bottom: 40%;
}

.homeCard {
    position: relative;
    border-radius: 5px;
    background-color: rgb(226, 224, 224);
    width: auto;
    column-count: 2;
    height: auto;
    marginX: auto;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
    background-size: 18px 18px;
    background-image: linear-gradient(
      -45deg,
      rgb(250, 245, 237) 25%,
      rgb(245, 240, 232) 25%,
      rgb(245, 240, 232) 50%,
      rgb(250, 245, 237) 50%,
      rgb(250, 245, 237) 75%,
      rgb(245, 240, 232) 75%,
      rgb(245, 240, 232) 100%
    );
    animation: pan 160s linear infinite;
}

@keyframes pan {
  0% {
    background-position: 0% 0%;
  }
  100% {
    background-position: 100% 0%;
  }
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
    width: 10vw;
    height: 20vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
}

.commingSoon {
    width: 90vh;
    padding: 90%;
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

@media (max-width: 800px) {
 .titleSection {
     width:auto;
     height:auto;
     padding:10%;
 }
 .title1 {
     text-align: left;
     font-size: 2vh;
     color: black
 }

 .title2 {
    text-align: left;
    font-size: 3vh;
    position: relative;
    color: black
 }

 .titleDescription {
   text-align: left;
   font-size: 1.2vh;
 }

 .homeCard {
    position: relative;
    border-radius: 5px;
    background-color: rgb(226, 224, 224);
    width: auto;
    column-count: 2;
    height: 60vh;
    marginX: auto;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
    transition: transform 0.3s ease-in-out; /* Add a smooth transition for scaling */
    background-size: 18px 18px;
    background-image: linear-gradient(
      -45deg,
      rgb(250, 245, 237) 25%,
      rgb(245, 240, 232) 25%,
      rgb(245, 240, 232) 50%,
      rgb(250, 245, 237) 50%,
      rgb(250, 245, 237) 75%,
      rgb(245, 240, 232) 75%,
      rgb(245, 240, 232) 100%
    );
    animation: pan 160s linear infinite;
 }

 .postOneButton {
    padding: 10%;
    position: relative;
    top: 10vh;
    background-color: white;
    border-radius: 10px;
 } 

 .imageSection {
    position: relative;
    border-radius: 5px;
    text-align: center;
    width: auto;
    height: 80vh;
    overflow: hidden;
    transform-origin: center center; /* Set the transform origin to the center */
 }
}
@media (min-width: 1024px) {
    .unavailbleText{
    font-size: 35px;
    color: rgb(0, 0, 0);
    position: relative;
    bottom: 150%;
}

.unavailbleBackground {
    font-size: 250px;
    color: rgb(211, 211, 211);
    position: relative;
    bottom: 40%;
}

.homeCard {
    position: relative;
    border-radius: 5px;
    background-color: rgb(226, 224, 224);
    width: auto;
    height: 70vh;
    overflow: hidden;
    marginX: auto;
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

.image {
    align-content: center;
    width: 100vw;
    height: 110%;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}

.imageSection {
    position: relative;
    border-radius: 5px;
    text-align: center;
    width: 40vw;
    height: 70vh;
    overflow: hidden;
    margin-bottom: 19px;
    transform-origin: center center; /* Set the transform origin to the center */
}

.commingSoon {
   width: 90vh;
    font-size:60px;
    animation: moveBackAndForth 20s ease-in-out infinite;
}

}
</style>
