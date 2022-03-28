<template>
  <div class="bg-[#EEF5F0] h-screen flex justify-center" @click="clicked">
    <audio id="music" src="/love-story.mp3" loop="loop" autoplay></audio>
    <div class="image1 w-screen md:w-[540px]" :class="animate && 'slide-out'">
      <div class="bg-[#EEF5F0] h-8 w-full absolute bottom-0" />
      <div class="bg-[#EEF5F0] w-2 absolute bottom-0 top-0 left-0" />
      <div class="bg-[#EEF5F0] w-2 absolute bottom-0 top-0 right-0" />
    </div>
    <div class="image2 w-screen md:w-[540px] relative">
      <a
        href="https://goo.gl/maps/xS2TU7zezv4hQx6q7"
        class="absolute bottom-[15%] left-[5%] top-[70%] right-[70%] z-10 hover:cursor-pointer"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',
  data: () => ({
    animate: false,
    play: false
  }),
  methods: {
    clicked() {
      ;(document.getElementById('music') as HTMLAudioElement).play()
      this.animate = true
    }
  }
})
</script>

<style scoped>
.image1 {
  position: absolute;
  top: 10%;
  bottom: 10%;
  background-image: url('/wedding31.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  z-index: 3;
  transition: transform ease-out 7000ms, opacity ease-out 1000ms,
    box-shadow ease-out 500ms;
}

.slide-out {
  transform: scale(0.4, 0.4) rotate3d(1, 2, 2, 30deg) translateX(300%);
  box-shadow: 22px 17px 41px 13px rgba(0, 0, 0, 0.64);
}

.image2 {
  position: absolute;
  top: 10%;
  bottom: 10%;
  background-image: url('/wedding32.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  z-index: 2;
}

@media (min-width: 540px) {
  .image2 {
    box-shadow: 22px 17px 41px 13px rgba(0, 0, 0, 0.64);
  }
}
</style>
