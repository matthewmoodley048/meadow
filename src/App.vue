<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';

</script>

<template>
  <div class="background">
   <div class="wrapper">
    <router-view v-slot="{Component}">
      <Transition name="page-opacity" mode="out-in">
        <component :is="Component"/>
      </Transition>
    </router-view>
   </div>
  </div>
  <NavBar msg="Meadow"/>
</template>

<style scoped>


.page-opacity-enter-active,
.page-opacity-leave-active {
 transition: 600ms ease all;
}

.page-opacity-enter-from,
.page-opacity-leave-to{
 opacity: 0;
 transform: translateY(60px)
}

.background{
  width: 100vw;
  position: fixed;
  background-size: 5px 5px;
  background-repeat: repeat;
  background-image: radial-gradient(white, rgba(0,0,0,0.1), white); 
  top: 0;
  left: 0;
  height: 100vh;
  animation: pan 120s linear infinite;
}

@keyframes pan {
  0% {
    background-position: 0% 0%;
  }
  100% {
    background-position: 100% 0%;
  }
}


.wrapper{
  margin-top:5vh;
  margin-left: 10vw;
  align-items: center;
  justify-content: center;  
  color: rgb(0, 0, 0);
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 2%;
  box-shadow: 0px 0px 0px 8px rgba(246,245,242,0.5);
  border-width: 100%;
  margin-top: 7vh;
  overflow-y: scroll;
  overflow-x: hidden;
  height: 80vh;
  width: 80vw;
}

*::-webkit-scrollbar {
  width: 0px; /* Adjust the width as needed */
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@font-face {
  font-family: 'Mooli';
  src: url('./assets/fonts/Croissant_One/CroissantOne-Regular.ttf') format('truetype');
}


</style>
