<template>
  <div class="bg-white">
    <h1 class="text-center p-5"> {{ contactInfo.title }} </h1>
    <section class="text-center p-10 text-2xl">
      <ul>
      <li class="p-4"><strong>Contact Number:</strong> 
        {{ contactInfo.number }}</li>
      <li class="p-4"><strong>Address:</strong> 
        {{ contactInfo.address }}</li>
      <li class="p-4"><strong>E-mail:</strong> 
        {{ contactInfo.email }}</li>
      </ul>
    </section>
    <section>
      <nuxt-content :contactInfo="contactInfo" />
      <Content v-for="member in members" :key="member.id" :contactInfo="member"></Content>
    </section>   
  </div>
</template>
<script>
export default {
  data(){
    this.$mail.send({
    to: 'jamesatkinson14@gmail.com'
  
    })}}
</script>