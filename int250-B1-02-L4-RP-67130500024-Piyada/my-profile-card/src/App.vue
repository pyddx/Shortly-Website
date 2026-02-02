<script setup>
import ProfileCard from "./components/ProfileCard.vue"
</script>

<template>
  <div class="flex items-center justify-center gap-8 min-h-screen bg-image bg-cover" :style="'background-image: url(./src/assets/bg-full.jpg)'">
  <ProfileCard 
  background="./src/assets/background-Be.jpg"
  profileimg="./src/assets/Profile-Be.png"
  name="Kritsanaphong Jaritpot"
  subheading="Student, 21, BKK"
  Contact="IG: mr.friendzone_sad"
  followers="395"
  following="1,262"
  projects="10+"
  />
  <ProfileCard 
  background="./src/assets/background-me.jpg"
  profileimg="./src/assets/Profile-me.png"
  name="Piyada Hanpayom"
  subheading="Student, 19, BKK"
  Contact="IG: _p.y.d"
  followers="503"
  following="412"
  projects="5+"
  />
  <ProfileCard 
  background="./src/assets/background-Ba.jpg"
  profileimg="./src/assets/Profile-Ba.png"
  name="Vanishaya Saephu"
  subheading="Student, 19, HKT"
  Contact="IG: b_.baimon_n"
  followers="406"
  following="311"
  projects="5+"
  />
  
  </div>
</template>

<style scoped></style>