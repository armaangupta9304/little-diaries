<template>
  <footer class="about">
      <div class="overflow"></div>
      <img class="about__image" width="4rem" src="../assets/lady.jpg" alt="">
      <div class="text_holder_footer">
          <span>About Me.</span>
          <h1>{{ About.title }}</h1>
          <p>{{ About.content }}</p>
      </div>
  </footer>
</template>

<script>
import About from "../dummy-about";

export default {
    data(){
        return {
            About: About.doc
        }   
    }
}
</script>

<style>
    .about{
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 30px;
        height: 100vh;
        position: relative;
    }
    .about__image {
        width: 30vw;
        height: 80vh;
        object-fit: cover;
        background-position: center;
        z-index: 5;
        position: relative;
    }
    .about__image::before{
        content: '';
        position: absolute;
        background-color: blue;
        border-radius: 50%;
        width: 300px;
        height: 300px;
        bottom: -100px;
        right: -100px;
    }
    .text_holder_footer {
        max-width: 500px;
        margin-left: 20px;
        z-index: 5;
    }
    .overflow{
        position: absolute;
        top: 0;
        left: 0;
        height: 100vh;
        width: 100%;
        background-color: rgba(255, 255, 255, 0.418);
    }
    .text_holder_footer h1 {
        position: relative;
        border-bottom: 1px solid black;
        z-index: 5;
    }
    .text_holder_footer p{
        z-index: 5;
    }
    .text_holder_footer h1::before{
        content: '';
        position: absolute;
        bottom: 0;
        width: 50%;
        height: 10%;
        right: 0;
        border: 1px solid black;
        background-color: rgb(193, 255, 93);
        z-index: 4;
    }
    .text_holder_footer p {
        background-color: transparent;
        box-shadow: 37px 40px 0px 10px rgb(232, 219, 137);
    }
    .text_holder_footer span {
        border-bottom: 1px solid black;
    }
    @media (max-width: 600px) {
        .text_holder_footer h1 {
            font-size: 20px;
        }
        .text_holder_footer p {
            font-size: 10px;
        }
    }
    @media (max-width: 500px) {
        .about {
            flex-direction: column;
            background-image: url("../assets/lady.jpg");
            background-color: rgba(255, 255, 255, 0.418);
            background-position: center;
            background-size: cover;
            background-blend-mode: multiply;
        }
        .about__image {
            display: none;
        }
        .text_holder_footer h1 {
            font-size: 50px;
            position: relative;
        }
        .text_holder_footer h1::before {
            display: none;
        }
        .text_holder_footer p {
            font-size: 20px;
            box-shadow: none;
        }
        
    }
</style>