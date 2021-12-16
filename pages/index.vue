<template>
<body>
  <section>
    <img src="/assets/stars.svg" alt="stars" id="stars">
    <img src="/assets/foreground_comet.png" alt="comet" id="comet">
    <img src="/assets/foreground_comet.png" alt="comet" id="comet2">
    <img src="/assets/background_planet.png" alt="planet_behind" id="planet_behind">    
    <img src="/assets/foreground_planet.png" alt="planet_front" id="planet_front">
    <h2 id="text">Jim Jam Super Site</h2>
    <a href="#" id="btn">See More</a>
  </section>
  <br>
  <main>
    <h1>head</h1>
    <ul>
      <li>item 1</li>
      <li>item 1</li>
      <li>item 1</li>
      <li>item 1</li>
      <li>item 1</li>
      <li>item 1</li>
    </ul>
  </main>
</body>  
</template>



<script>
  export default {  
    mounted() {
        this.staggering()
      },
      methods: {
        staggering() {
          const anime = this.$anime
          anime({
            targets: '#planet_behind, #planet_front, #comet, #comet2',
            translateY: [6000, -250],
            delay: anime.stagger(200, {from:'center'})
          })
        }
      }};
</script>



<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900&display=swap');

section {
  position: relative;
  width: 100%;
  max-width: 2000px;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
} 

section img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  pointer-events: none;
}

section img#stars {
  object-fit: cover;
  width: auto;
  height:  100%;
}

section > #planet_behind {
  top: initial;
  width: 70%;
  max-width: 700px;
}

section > #planet_front {
  bottom: initial;
  width: 70%;
  max-width: 700px;
  top: 50%;
  left: 20%;
}

section img#comet {
  top: initial;
  width: 20%;
  max-width: 300px;
  bottom: 60%;
  left: 65%;
}

section img#comet2 {
  top: initial;
  width: 10%;

  bottom: 57%;
  left: 70%;
}

#text {
  position: relative;
  top: 20%;
}

#text span {
  font-weight: 700;
}

#btn {
  position: absolute;
  top: 70%;
  left: 50%;
  transform: translate(-50%, 50%);
  text-decoration: none;
  display: inline-block;
  padding: 8px 50px;
  background: #fff;
  border-radius: 40px;
  font-size: 1.4em;
  color: #2b1055;
  z-index: 10000;
}
</style>