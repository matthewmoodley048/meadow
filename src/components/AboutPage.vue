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
                Meadow was created by <a href="https://www.linkedin.com/in/matthew-moodley-148072235?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app">me </a> as a platform to document topics I have explored or am currently exploring, as well as to discuss projects I have completed. 
            </p>
      <p class="body">
      Through Meadow, both you, the reader, and I can learn together about various computer-related topics and how knowledge, passion, and enjoyment can empower us to create our own beautiful creations.      
           </p>
        </div>
    </div>
</template>

<style scoped>
    .container {
       width:auto;
       height:100vh;
       display: flex;
        margin: auto;
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
        margin-top:10px;
        margin-bottom: 20px;
    }

    .textContainer {
        text-align: left;
    }

    h1 {
        margin-top:10px;
        font-weight: 500;
        font-size: 3vh;
    }

    .body {
        white-space: pre-wrap;
        font-size: 2vh;
        padding:1vh 10vw;
    }

</style>

