<template>
  <li>
    <ul>
      <li class="G1">Item1</li>
      <li class="G2">Item2</li>
    </ul>
    <ul>
      <li class="G3">Item3</li>
      <li class="G4">Item4</li>
    </ul>
  </li>
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
        targets: "#G1, #G2",
        translateY: [6000, -250],
        delay: anime.stagger(200, { from: "center" }),
      });
      anime({
        targets: "#G3, #G4",
        translateY: [6000, -250],
        delay: anime.stagger(200, { from: "center" }),
      });
    },
  },
};
</script>

<style>
#G1, #G2, #G3, #G4 {
  height:60%;
  width: 100%;
  object-fit: cover;
  background-color: purple;
}

</style>