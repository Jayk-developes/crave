<script setup lang="ts">

let windowWidth = screen.width + "px"
let windowHeight = screen.height + "px"

let testPhotoNames: string[] = ["pic1.jpg", "pic2.jpg", "pic3.jpg", "pic4.jpg", "pic5.jpg"]

const getImageURL = ((name: string) => {
  return new URL(`../testmedia/${name}`, import.meta.url).href
})

</script>

<template>
  <div class="fullContent" dir="ltr">
    <div class="content" v-for="pic in testPhotoNames">
      <img :src="getImageURL(pic)" :alt="pic" class="fitImage">
    </div>
  </div>
</template>

<style scoped>
.content {
  position: relative;
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 90%;
  height: 100%;
  margin: 10rem 5%;
  margin-left: 5%;
  background-color: #1116;
  border-radius: .5rem;
  scroll-snap-align: center;
}

.fullContent {
  overflow-y: hidden;
  display: flex;
  flex-direction: column;
  gap: 10rem;
  scroll-snap-points-y: repeat(auto-fit, 100vh);
  scroll-snap-type: y mandatory;
}

.fitImage {
  width: 100%;
}
</style>