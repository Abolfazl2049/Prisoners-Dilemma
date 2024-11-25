<script setup lang="ts">
let loopVideo: any;
onMounted(() => {
  loopVideo = setInterval(() => {
    document.getElementById("opening-video")?.play();
  }, 8000);
});
onUnmounted(() => {
  clearInterval(loopVideo);
});
</script>
<template>
  <div class="relative h-[100vh] w-[100%]">
    <DocumentInfo> some text </DocumentInfo>
    <div class="flex-center absolute inset-0 z-[10]">
      <div class="btn-con">
        <div class="hover:bg-white hover:text-[black]">Leaderboard</div>
        <div
          class="!border-[#FEFF1E] bg-[#FEFF1E] !text-black hover:text-[23px]"
          @click="navigateTo('/play')"
        >
          Play
        </div>
        <div class="hover:bg-white hover:text-[black]">Profile</div>
      </div>
    </div>
    <video
      autoplay
      muted
      src="/videos/opening-video.mp4"
      id="opening-video"
      class="h-[100%] w-[100%] object-fill"
    ></video>
  </div>
</template>
