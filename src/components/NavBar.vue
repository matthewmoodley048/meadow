<script setup lang="ts">
defineProps<{
  msg: string
}>()

</script>

<template>
  <div class="greetings">
    <nav class="nav">
        <RouterLink class="navItems" to="/">Home</RouterLink>
         |
        <RouterLink  class="navItems" to="/about">About</RouterLink>
    <h1> {{ msg }}</h1>
    </nav>

  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2rem;
  position: fixed;
}

h3 {
  font-size: 1.2rem;
}
.greetings h1,
.greetings h3 {
  top: 90%;
  position: absolute;
  flex-direction: column;
  text-align: center;
  width: 15%;
  border-radius: 13px;
  text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
  color: rgb(0, 0, 0);
}

.nav{
  position: absolute;
  overflow: hidden;
  text-align: center;
    padding: 1%;
    width: 15%;
    border-radius: 13px;
    text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
color: rgb(0, 0, 0);
}
.navItems{
  color: rgb(0, 0, 0);
  margin: 2%;
}
</style>
