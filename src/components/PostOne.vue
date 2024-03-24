<script setup lang="ts">


</script>

<template>
  <div class="header">

    <h1>Place holder page!</h1>
    <iframe src="https://giphy.com/embed/l3vRlT2k2L35Cnn5C" class="gif"  allowFullScreen></iframe>

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
.gif{
  bottom:50%;
  left: 20%;
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
./CoverObject.js