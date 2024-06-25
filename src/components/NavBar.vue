<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
<div class="nav">
  <nav  tabs type="dark" variant="dark">
   <RouterLink class="brand" to="/">{{msg}}</RouterLink>
   <RouterLink class="navItems" to="/">Home</RouterLink>
   <RouterLink class="navItems" to="/about" disabled>About</RouterLink>
  </nav>
</div>
</template>

<style scoped>

.nav {
   top: 0;
   left: 0;
   display: flex;
   justify-content: flex-start;
   align-items: stretch;
   overflow: hidden; 
   position: fixed;
   text-align: center;
   padding: 1%;
   width: 100vw;
   border-radius: 13px;
}

.brand {
  left: 0;
  margin-right: 25%;
}

.navItems {
  color: black.500;
  margin-left: 2%;
  padding: 10%;
}

</style>
