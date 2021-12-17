<template>
  <header class="header">
    <img src="assets/JWebb.svg" alt="logo" class="logo">
    <ul>      
      <li>
        <nuxt-link to='/'>Home</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{path: '/', hash: '#projects'}">Projects</nuxt-link>
      </li>     
      <li>
        <nuxt-link :to="{path: '/', hash: '#about'}">About</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{path: '/', hash: '#contact'}">Contact</nuxt-link>
      </li>      
    </ul>
        
  </header>  
</template>

<script>
export default {
  name: 'AppHeader', 
}
</script>

<style>
.logo {
  width: auto;  
  height: 100px;
}
  .header {
    display: flex;
    justify-content: center;
    align-items:center;
    background: transparent;
    margin-bottom: 1rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid grey;
} 
  .header .title {
  font-size: 3rem;
  color: #5d6c8a;
}
  .header ul {
    display: flex;
}
  .header a {
    display: inline-block;
    background: transparent;
    color: white;
    font-size: 1em;
    padding: 0.3rem 1rem;
    margin-right: 0.5rem;
}
</style>