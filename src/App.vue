<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';

</script>

<template >
   <div class="wrapper">
  <NavBar msg="Meadow"/>
    <router-view v-slot="{Component}">
      <Transition name="page-opacity" mode="out-in">
        <component :is="Component"/>
      </Transition>
    </router-view>
   </div>
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

.wrapper{
position: absolute;
  align-content: center;
  color: rgb(0, 0, 0);
  background-color: rgba(255, 255, 255, 0.4);
  border-color: rgba(255, 255, 255, 0.2);
  border-radius: 2%;
  border-width: 10px;
  top: 45vh;
  left: 50vw;
  transform: translate(-50%, -50%);
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1), inset 0px 0px 2px 3px rgba(0,0,0,0.1);
  overflow-y: scroll;
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

@media (min-width: 1024px) {
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
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.05), inset 0px 0px 2px 3px rgba(0,0,0, 0,1) ;
}

}
</style>
