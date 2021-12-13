<template>
  <div>
    <h1>About Me</h1>
    <p>For anyone that cares...</p>
    <br>
    <div class="about">
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
          content: "About Me",
        },
      ],
    };
  },
};
</script>

<style>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-width: 400px;
}
</style>