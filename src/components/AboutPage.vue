<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="header">
    <h1>{{ msg }}</h1>
    <Vue3Lottie
        animation-link="https://lottie.host/e61776d9-b413-4876-b5e3-c5901d498984/Qy7A5ObqVj.json"
        :height="400"
        :width="400"
        :scale="1"
        direction="alternate"
    />
    <p data-value="This is a blog post" class="body">
      Meadow is a note book logging interesting topics and projects i have made.
    </p>
  </div>

</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.header h1,
.header h3 {
  left: 30%;
  text-align: center;
  position: fixed;
  animation: fade 700ms ease-in-out;
}


.body {
  white-space: pre-wrap; /* Prevent text from wrapping */
  overflow: hidden; /* Hide overflowed characters */
  font-size: 24px;
  padding: 5%;
  position: relative;
  animation: fade 1s ease-in-out; /* Adjust duration as needed */
}

@keyframes fade{
  from {
    color: aliceblue;
  }
  to {
    color: black;
  }
  
}

@media (min-width: 1024px) {
  .header h1,
.header h3 {
  left: 30vw;
  text-align: center;
  position: fixed;
  animation: fade 700ms ease-in-out;
}
  .body  {
    padding: 5%;
    white-space: pre-wrap; /* Prevent text from wrapping */
    overflow: hidden; /* Hide overflowed characters */
    font-size: 24px;
    position: relative;
    animation: fade 1s ease-in-out; /* Adjust duration as needed */
 }
}
</style>
