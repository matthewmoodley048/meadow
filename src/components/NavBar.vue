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
  position: fixed;
  flex-direction: column;
  text-align: center;
  width: 15%;
  border-radius: 13px;
  text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
  color: rgb(0, 0, 0);
}

.nav{
  position: fixed;
  top: 90%;
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
@media (min-width: 1024px) {

  .greetings h1,
.greetings h3 {
  top: 90%;
  left: 43%;
  position: fixed;
  flex-direction: row;
  text-align: center;
  width: 15%;
  border-radius: 13px;
  text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
  color: rgb(0, 0, 0);
}

.nav{
  position: fixed;
  flex-direction: row;
  top: 95%;
  left: 43%;
  text-align: center;
    padding: 1%;
    width: 15%;
    border-radius: 13px;
    text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
    color: rgb(0, 0, 0);
}
.navItems{
  margin: 2%;
}
}
@media (max-width: 700px) {     .greetings h1,
.greetings h3 {
  position:  relative;
  flex-direction: row;
  width: 100%;
  border-radius: 13px;
  text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
  color: rgb(0, 0, 0);
}

.nav{
    padding: 1%;
    width: 85%;
    text-align: center;
    border-radius: 13px;
    text-shadow: 4px 3px 1px rgba(0, 0, 0, 0.15);
    color: rgb(0, 0, 0);
}
.navItems{
  margin: 2%;
}}
</style>
