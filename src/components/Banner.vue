<template>
  <div class="hero__banner">
      <div class="row">
          <div class="row_content">
              <h1 class="primary_text">Woo Hoo!</h1>
              <div class="image_container">
                <img width="300" src="../assets/nature_undraw.svg" alt="">
              </div>
              <div class="image__container__cloud">
                  <img width="300" src="../assets/clouds.svg" alt="">
              </div>
          </div>
          <div class="cols">
            <div class="col col1">
                <h1>Little Diaries</h1>
            </div>
            <div class="col col2">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem voluptas unde, praesentium itaque iusto voluptate distinctio nobis molestias aperiam pariatur et eaque iure?</p>
            </div>
          </div>
      </div>
      <a href="#blogs" class="down_arrow_container">
        <i class="fas fa-arrow-down"></i>
      </a>
  </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style>
.hero__banner img {
    animation: animateOpacity 0.5s linear;
}
.center{
    display: flex;
    align-items: center;
    justify-content: center;
}
.hero__banner{
    height: 100vh;
    width: 100%;
}
.image_container{
    position: absolute;
    bottom: 60px;
    left: 60px;
}
.image__container__cloud {
    position: absolute;
    top: 40px;
    right: 40px;
}

.row{
    display: flex;
    align-items: center;
}
.row_content{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #f7f6e7;
    height: 100vh;
    width: 70%;
    background-color: #314e52;
    position: relative;
}

.col1{
    background-color: #f2a154;
    color: #314e52;
}
.col2{
    background-color: #f7f6e7;
    color: #314e52;
}
.col2 p {
    max-width: 60%;
}
.cols{
    height: 100vh;
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.cols .col{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.primary_text {
    font-size: 70px;
}
.down_arrow_container{
    position: absolute;
    bottom: 10px;
    right: 10px;
    color: #3f3f3f;
    text-decoration: none;
    font-size: 40px;
    animation: animateDown 2s linear;
}
@media (max-width: 800px) {
    .row{
        flex-direction: column;
    }
    .row_content{
        height: 70vh;
        width: 100%;
    }
    .cols {
        flex-direction: row;
        height: 30vh;
        width: 100%;
    }
    .image_container{
        display: none;
    }
}
@media (max-width: 687px) {
    .cols {
        flex-direction: column;   
    }
    .row_content {
        height: 80vh;
    }
    .cols {
        height: 20vh;
    }
    .col.col2 {
        display: none;
    }
    .col.col1{
        height: 100%;
    }
}
@keyframes animateDown {
    0% {
        bottom: 10px;
    }
    25% {
        bottom: 50px;
    }
    50% {
        bottom: 10px;
    }
    75% {
        bottom: 50px;
    }
    100% {
        bottom: 10px;
    }
}
@keyframes animateOpacity {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
</style>