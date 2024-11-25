<template>
  <documentInfo> some text </documentInfo>
  <div class="img-game-type-selection flex-center relative h-[100vh] w-[100%]">
    <div class="btn-con">
      <div
        class="relative before:absolute before:-right-9 before:-top-3 before:h-[32px] before:rounded-lg before:bg-[red] before:px-1 before:pt-[7px] before:text-center before:text-[11px] before:content-['coming-soon'] hover:bg-white hover:text-black hover:before:text-white"
      >
        Multiplayer
      </div>
      <div
        class="hover:bg-white hover:text-black"
        @click="navigateTo('/play/single')"
      >
        Singleplayer
      </div>
    </div>
  </div>
</template>
