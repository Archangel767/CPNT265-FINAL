<template>
  <div class="container">
    <AppHeader />
    <nuxt />    
    <AppFooter />
  </div>
</template>

<script>
export default {
  
};
</script>

<style>
* {
  scroll-behavior: smooth;
  margin: 0;
  padding: 0%, 20%;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
body {
  min-width:100vw;
  font-family: Arial, Helvtica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  min-height: 100vh;
  background: linear-gradient(#211953, #604a8d);
}
a {
  color: #666;
  text-decoration: none;
}
ul {
  list-style: none;
}
.container {
  max-width: 1200px;
  margin: 2rem 0rem;
  overflow: hidden;
}
</style>
