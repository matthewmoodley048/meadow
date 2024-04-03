<script setup lang="ts">
    defineProps<{
        msg: string
    }>()
</script>

<template>
    <div class="container">
    <h1>{{msg}}</h1>
    <div class="imageContainer"></div>
        <div class="textContainer">
            <p class="body">
            Meadow was created by me as a platform to document topics I have explored or am currently exploring, as well as to discuss projects I have completed. 
            </p>
      <p class="body">
      Through Meadow, both you, the reader, and I can learn together about various computer-related topics and how knowledge, passion, and enjoyment can empower us to create our own beautiful creations.      
           </p>
        </div>
    </div>
</template>

<style scoped>
    .container {
        display: flex;
        margin: 0 auto;
        padding: 0;
        flex-direction: column;
        align-items: center;
    }

    .imageContainer {
        width: 50vh;
        height: 50vh;
        overflow: hidden;
        background: url('../assets/images/aboutImage.jpg') no-repeat center;
        background-size: contain;
        border-radius: 0px;
        box-shadow: inset 0px 0px 10px 50px #f2f2f2, 0px 0px 10px 10px #f2f2f2;
        animation: fade 1.5s ease-in-out;
        margin-bottom: 20px;
    }

    .textContainer {
        text-align: left;
        animation: fade 1.7s ease-in-out;
    }

    h1 {
        font-weight: 500;
        font-size: 3vh;
        animation: fade 1s ease-in-out;
    }

    .body {
        white-space: pre-wrap;
        font-size: 2vh;
        padding:1vh 10vw;
    }

    @keyframes fade {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
</style>

