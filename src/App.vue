<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';

</script>

<template >
    <!-- <img src='./components/images/village.jpg' class="image" /> -->
  <div class="wrapper">
    <RouterView/>
  </div>
  <NavBar msg="Meadow"/>
</template>

<style scoped>

header {
  line-height: 1.5;
  max-height: 100vh;
}


.image{
  position: absolute;
  width: 100vw;
  height: 100vh;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}
.wrapper{
  align-content: center;
  color: rgb(0, 0, 0);
  position: fixed;
  background-color: rgba(255, 255, 255, 0.4);
  border-color: rgba(255, 255, 255, 0.2);
  border-radius: 2%;
  border-width: 10px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  box-shadow: 0px 0px 5px 10px rgba(0, 0, 0, 0.1), inset 0px 0px 2px 3px rgba(0,0,0,0.1);
  overflow-x: hidden;
  scrollbar-width: 200%;
  overflow-y: scroll;
  height: 80%;
  width: 85vw;
  border-style:ridge;
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

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .wrapper{
  position: fixed;
  background-color: rgba(255, 255, 255, 0.4);
  border-color: rgba(255, 255, 255, 0.2);
  border-radius: 5px;
  border-width: 90%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  overflow-x: hidden;
  scrollbar-width: 200%;
  overflow-y: scroll;
  height: 80%;
  width: 85vw;
  box-shadow: 0px 0px 5px 10px rgba(0, 0, 0, 0.05), inset 0px 0px 2px 3px rgba(0,0,0, 0,1) ;
  border-style:ridge;
}

  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
