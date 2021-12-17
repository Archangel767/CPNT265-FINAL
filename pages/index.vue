<template>
<body>
  <section>
    <img src="/assets/stars.svg" alt="stars" id="stars">
    <img src="/assets/foreground_comet.png" alt="comet" id="comet">
    <img src="/assets/foreground_comet.png" alt="comet" id="comet2">
    <img src="/assets/background_planet.png" alt="planet_behind" id="planet_behind">    
    <img src="/assets/foreground_planet.png" alt="planet_front" id="planet_front">
    <div id="lineDrawing">
        <svg viewBox="0 0 792 512">
        <g class="lines">
        <!-- J --> <path class="my-path" d="M35.63,65.47c-3.16,15.07-7.69,22.14-22.89,22.14A43.63,43.63,0,0,1,1.5,86.31L4.29,73.39a20.71,20.71,0,0,0,4.9.5c4.92,0,6.6-1.5,8.16-8.79l10-47H45.73Z"/>
        <!-- A --><path class="my-path" d="M63.3,72.47,56.86,86.6H38.08C45,72.91,62.58,35.12,71.28,18.12H96l5,68.48H82.7l-.8-14.13ZM82,58.2c-.48-10.3-1-20.76-.81-27.82H80.8C77.81,38.3,73.64,48.15,69,58.2Z"/>
        <!-- M --><path class="my-path" d="M165.84,64.43c2.26-10.63,5.53-25.15,7.6-33.27h-.63C167.16,46,157.38,68.81,149.65,86.6H134.12c.51-18.27.78-40.35,1.34-55.43h-.63c-1.17,8-3.83,22-6.33,33.8L123.92,86.6H107.7l14.53-68.48h25.92c.14,12.37.13,33.55-.32,43.52h.35C152,50.91,160.49,32.88,167,18.12h26.32L178.81,86.6H161.17Z"/>
        <!-- E --><path class="my-path" d="M243.43,58.36H216l-3.07,14.52h32.4L240.6,86.6H192.3l14.53-68.48h46.28l-3,13.83H221.59l-2.71,12.59h27.47Z"/>
        <!-- S --><path class="my-path" d="M269.81,66.11c.59,5.28,3.25,9.19,9.61,9.19,5.28,0,8.35-2.6,8.35-7.44,0-4.51-2.27-6.59-10.09-10-13-5.55-18.32-10.53-18.32-19.82,0-11.69,8.52-21.18,25.47-21.18,17.86,0,25.8,9.77,25.7,20.94H293.07c-.36-4.36-2.2-8.33-8.35-8.33-4.78,0-6.8,2.58-6.8,6.08s2.41,5.23,9.87,8.29C303.3,50.26,307,56.74,307,65c0,13.53-9.92,22.86-28.42,22.86-18.7,0-26.21-9.81-26.37-21.77Z"/>
        </g>
        </svg>  
    </div>      
  </section>

  <section id="about">
       <h1>About</h1>
    <ul>
      <li>Item1</li>
    </ul>
  </section>
  <section id="projects">
    <h1>Projects</h1>
    <ul>
      <li>Item1</li>
      <li>Item2</li>
      <li>Item3</li>
      <li>Item4</li>
    </ul>
    </section>
    <section>
    <h1 id="contact">Contact Details</h1>
    <ul>
      <li>Item1</li>
      <li>Item2</li>
      <li>Item3</li>
      <li>Item4</li>
    </ul>
      </section>
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
            targets: '#planet_behind, #planet_front, #comet, #comet2, #linedrawing',
            translateY: [6000, -250],
            delay: anime.stagger(200, {from:'center'})
          })
          var lineDrawing = anime({
            targets: '#lineDrawing .lines path',
            strokeDashoffset: [anime.setDashoffset, 0],
            easing: 'easeInOutSine',
            duration: 2000,
            delay: function(el, i) { return i * 250 },
            direction: 'alternate',
            loop: false
          });
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
  background: rgb(158, 122, 122);
  border-radius: 40px;
  font-size: 1.4em;
  color: #2b1055;
  z-index: 10000;
}

.my-path {
  fill:none;
  stroke:#733acf;
  stroke-width:4;
}

#lineDrawing {
  position: absolute;
  bottom: 50%;
  left: 65%;
}
</style>