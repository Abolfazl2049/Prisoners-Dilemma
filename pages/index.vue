<script setup>
import {ref, onMounted} from "vue";
let uiStateManager = ref({
  oppeningImg: false
});
let videoOppening = ref();
onMounted(() => {
  setInterval(() => {
    uiStateManager.value.oppeningImg = false;
    videoOppening.value.classList.remove("hidden");
    videoOppening.value.play();
    setTimeout(() => {
      uiStateManager.value.oppeningImg = true;
      videoOppening.value.classList.add("hidden");
    }, 1650);
  }, 7000);
  setTimeout(() => {
    uiStateManager.value.oppeningImg = true;
    videoOppening.value.classList.add("hidden");
  }, 1650);
});
</script>
<template>
  <div class="w-[100%] h-[100vh] relative">
    <img
      src="/imgs/questionMark.png"
      class="hover:scale-[1.1] transition-all cursor-pointer absolute w-[60px] z-[20]"
      alt=""
    />
    <img
      src="/imgs/Oppening-img2.jpg"
      style="object-fit: fill"
      class="h-[100%] w-[100%] absolute z-[0]"
      alt=""
      v-if="uiStateManager.oppeningImg"
    />
    <div class="absolute bg-[rgba(255,255,255,0.10)] inset-0">
      <div
        class="*:m-2 *:w-[100%] *:h-[75px] *:border-[4px] *:transition-all *:border-white *:cursor-pointer *:text-[20px] *:text-center *:pt-[22px] flex flex-col mx-auto w-[clamp(250px,50%,600px)] mt-[30vh] items-center"
      >
        <div class="hover:bg-white text-white hover:text-[black]">
          Leaderboard
        </div>
        <div class="hover:bg-white hover:text-black">Play</div>
        <div class="hover:bg-white text-white hover:text-[black]">Profile</div>
      </div>
    </div>
    <video
      autoplay
      muted
      src="/videos/Oppening-video2.mp4"
      ref="videoOppening"
      style="object-fit: fill"
      class="h-[100%] w-[100%]"
    ></video>
  </div>
</template>
