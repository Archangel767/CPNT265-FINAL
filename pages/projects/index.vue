<template>
  <div>
    <h1>My Projects</h1>
    <p>If I had any...</p>
    <br>
    <div class="gallery">
      <nuxt-img src="/chuckle.jpeg" sizes="sm:100px md:200px lg:400px" />
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "My Projects'",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "gallery of current projects",
        },
      ],
    };
  },
};
</script>

<style>
.gallery {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-width: 400px;
}
</style>