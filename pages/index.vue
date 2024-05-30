<script setup>
import { ref, onMounted } from "vue";
let videoOppening = ref();
onMounted(() => {
  setInterval(() => {
    videoOppening.value.play();
  }, 20000);
});
</script>
<template>
  <div class="relative h-[100vh] w-[100%]">
    <img
      src="/imgs/questionMark.png"
      class="absolute z-[20] w-[60px] cursor-pointer transition-all hover:scale-[1.1]"
    />
    <div class="flex-center absolute inset-0 z-[10] bg-[rgba(190,149,149,0.1)]">
      <div
        class="flex w-[clamp(250px,50%,600px)] flex-col items-center *:m-2 *:h-[75px] *:w-[100%] *:cursor-pointer *:border-[4px] *:border-white *:text-center *:text-[20px] *:transition-all"
      >
        <div class="flex-center text-white hover:bg-white hover:text-[#d06767]">
          Leaderboard
        </div>
        <div
          class="flex-center !border-[#FEFF1E] bg-[#FEFF1E] transition-all hover:text-[23px]"
        >
          Play
        </div>
        <div class="flex-center text-white hover:bg-white hover:text-[black]">
          Profile
        </div>
      </div>
    </div>
    <video
      autoplay
      muted
      src="/videos/oppening_video.mp4"
      ref="videoOppening"
      class="h-[100%] w-[100%] object-fill"
    ></video>
  </div>
</template>
