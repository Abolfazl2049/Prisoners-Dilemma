<script setup>
onMounted(() => {
  setInterval(() => {
    document.getElementById("videoOppening").play();
  }, 20000);
});
</script>
<template>
  <div class="relative h-[100vh] w-[100%]">
    <DocumentInfo> some text </DocumentInfo>
    <div class="flex-center absolute inset-0 z-[10]">
      <div class="button_container">
        <div class="hover:bg-white hover:text-[#f9d9d9]">Leaderboard</div>
        <div
          class="!border-[#FEFF1E] bg-[#FEFF1E] !text-black hover:text-[23px]"
        >
          Play
        </div>
        <div class="hover:bg-white hover:text-[black]">Profile</div>
      </div>
    </div>
    <video
      autoplay
      muted
      src="/videos/oppening_video.mp4"
      id="videoOppening"
      class="h-[100%] w-[100%] object-fill"
    ></video>
  </div>
</template>
