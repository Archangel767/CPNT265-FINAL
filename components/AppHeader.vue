<template>
  <header class="header">
    <ul>
      <li>
        <nuxt-link to='/'>Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to='/projects'>Projects</nuxt-link>
      </li>      
      <li>
        <nuxt-link to='/about'>About</nuxt-link>
      </li>
      <li>
        <nuxt-link to='/contact'>Contact</nuxt-link>
      </li>      
    </ul>
        
  </header>  
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>
<style>
  .header {
    display: flex;
    justify-content: center;
    align-items:center;
    background: #778188;
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