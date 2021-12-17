<template>
  <section id="grid-container">
    <ul>
      <li>
        <figure>          
          <img src="#" alt="Profile pic">
        </figure>        
      </li>
      <li>
        <figure>
          <figcaption><h3>Billions upon billions</h3></figcaption>
        </figure>
        <p>
          Made in the interiors of collapsing stars star stuff harvesting star light venture billions upon billions Drake Equation brain is the seed of intelligence?
        </p>
        <a href="#">Visit Website</a>
      </li>
    </ul>  
  </section>    
</template>

<script>
export default {

};
</script>

<style>
#grid-container {
  display: grid;
  align-items: start; 
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  grid-gap: 1rem;
  padding: 2rem;
}

#grid-container > ul > li {
  border: 1px solid #E2E2E2;
  border-radius: .5rem;
}

#grid-container > ul > li > figure {
  min-height: 220px;
  overflow: hidden;
  border-top-left-radius: .5rem;
  border-top-right-radius: .5rem;
  position: relative;
}

#grid-container > ul > li > figure > img {
  width: 100%;
}

#grid-container > ul > li > figure > figcaption {
  position: absolute;
  bottom: 0;
  background-color: rgba(0,0,0,.7);
  width: 100%;
}

#grid-container > ul > li > figure > figcaption > h3 {
  color: white;
  padding: .75rem;
  font-size: 1.25rem;
}
</style>