<template>
  <div class="container">
    <AppHeader />
    <nuxt />
    <AppFooter />
  </div>
</template>

<script>
export default {
  
}
//   import AppHeader from '../components/AppHeader';
//   import AppFooter from '../components/AppFooter';
//   export default {
//     components: {
//       AppHeader,
//       AppFooter
//     }
    
// }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
  }
  body {
    font-family: Arial, Helvtica, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    min-height: 100vh; 
    background: linear-gradient(#261e53, #604a8d);
  }
  a {
    color: #666;
    text-decoration: none;
  }
  ul {
    list-style: none;
  }
.container {
  max-width: 90%;
  margin: 2rem auto;
  overflow: hidden;
}
</style>
