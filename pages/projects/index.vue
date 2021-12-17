<template>
  <figure>
    <img src="assets/JWebb.svg" alt="G1" class="G1">
    <img src="assets/JWebb.svg" alt="G2" class="G2">
    <br>
    <img src="assets/JWebb.svg" alt="G3" class="G3">
    <img src="assets/JWebb.svg" alt="G4" class="G4">
    <br>
    <img src="assets/JWebb.svg" alt="G5" class="G5">
    <img src="assets/JWebb.svg" alt="G6" class="G6">
  </figure>
</template>

<script>
export default {
  mounted() {
    this.staggering();
  },
  methods: {
    staggering() {
      const anime = this.$anime;
      anime({
        targets: ".G1, .G2 ",
        translateX: '20rem',
        rotate: 180,
        borderRadius: '8px',
        duration: 1500,
        loop: false,
      });
      anime({
        targets: ".G3, .G4",
        translateX: '20rem',
        translateY: '0rem',
        rotate: 180,
        borderRadius: '8px',
        duration: 2000,
        loop: false      
      });
      anime({
        targets: ".G5, .G6",
        translateX: '20rem',
        translateY: '0rem',
        rotate: 180,
        borderRadius: '8px',
        duration: 2500,
        loop: false      
      });
    },
  },
};
</script>

<style>

figure {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;    
    text-align: center;
  }



.G1, .G2   {
  position: relative;
  text-align: center;
  color: white; 
  width: 18rem;
  height: 18rem;
  margin: .5rem;
  background-color: purple;
  border: 1px solid black;
  top: initial;  
  margin-top: 5%;
  
}

.G3, .G4 {
  position: relative;
  text-align: center;
  color: white; 
  width: 18rem;
  height: 18rem;
  margin: .5rem;
  background-color: purple;
  border: 1px solid black;
  top: initial;
  margin-top: 5%;
}

.G5, .G6 {
  position: relative;
  text-align: center;
  color: white; 
  width: 18rem;
  height: 18rem;
  margin: .5rem;
  background-color: purple;
  border: 1px solid black;
  top: initial;
  margin-top: 5%;
}


</style>