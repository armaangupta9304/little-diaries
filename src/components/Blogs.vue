<template>
  <div class="blogs__holder" id="blogs">
      <div v-for="blog of data.doc" :key="blog._id" class="blog">
          <div class="blog_date_title">
            <div class="blog_title">
                <h1> {{ blog.title }} </h1>
            </div>
            <div class="blog_date">
                {{ blog.createdAt }}
            </div>
          </div>
          <div class="blog_content">
              <p>{{ blog.content.substring(0, 100) + "..." }}</p>
              <a href="#" class="read_more">Read More...</a>
          </div>
      </div>
  </div>
</template>

<script>
import data from "../dummy-data";

export default {
    name: 'Blog',
    data(){
        return {
            data: data
        }
    }
}
</script>

<style>
    .blogs__holder{
        min-height: 100vh;
        width: 100%;
    } 
    .blog{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 50px;
    }
    .blog .blog_date_title, .blog_content{
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 60%;
    }
    .blog .blog_date_title {
        margin-bottom: 24px;
    }
    .blog_title{
        justify-self: flex-start;
    }
    .blog_content p {
        max-width: 40%;
    }
    .read_more {
        background-color: #1687a7;
        color: white;
        padding: 30px;
        border-radius: 12px;
        transition: background-color 0.5s ease-in;
    }
    .read_more:hover {
        background-color: #12647a;
    }
    .blog_content {
        border: 1px solid black;
        border-radius: 12px;
        padding: 30px;
    }

    @media (max-width: 1000px) {
        .blog .blog_date_title {
            flex-direction: column;
            align-items: unset;
            align-items: flex-start;
            justify-content: flex-start;
            margin-bottom: 24px;
            border-bottom: 1px solid black;
        }
    }
    @media (max-width: 700px) {
        .blog .blog_date_title, .blog_content {
            width: 100%;
        }
    }
    @media (max-width: 500px) {
        .blog .blog_content {
            flex-direction: column;
        }
        .blog_content * {
            width: 100%;
        }
        .blog_content p{
            max-width: unset;
        }
    }
</style>