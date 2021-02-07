<template>
  <Banner />
  <Blogs />
  <Footer />
</template>

<script>
import Banner from "./components/Banner";
import Blogs from "./components/Blogs";
import Footer from "./components/Footer";
export default {
  name: 'App',
  components: {
    Banner,
    Blogs,
    Footer
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
::-webkit-scrollbar {
  width: 0px;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins";
}
</style>
