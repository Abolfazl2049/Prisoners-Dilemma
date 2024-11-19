<script setup>
let bot_list = ref([
  {
    name: "Tit for tat",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "tit-for-tat",
    hover: false,
  },
  {
    name: "Joss",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "joss",
    hover: false,
  },
  {
    name: "Tit for two tat",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "tit-for-two-tat",
    hover: false,
  },
  {
    name: "Suspicious",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "suspicious",
    hover: false,
  },
  {
    name: "Pavlov",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "pavlov",
    hover: false,
  },
  {
    name: "Grim trigger",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "grim-trigger",
    hover: false,
  },
  {
    name: "AlwaysD",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "alwaysD",
    hover: false,
  },
  {
    name: "AlwaysC",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "alwaysC",
    hover: false,
  },
  {
    name: "Random",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "random",
    hover: false,
  },
]);
</script>
<template>
  <div class="bg_img_bot h-[100vh] overflow-y-scroll py-10">
    <DocumentInfo> some text </DocumentInfo>
    <div
      class="mx-auto flex h-fit w-[clamp(300px,70%,900px)] flex-col transition-all hover:max-h-[300px]"
    >
      <p
        class="mx-auto mb-2 w-full text-[20px] text-white before:content-['#']"
      >
        choose your Opponent !
      </p>
      <div
        id="card"
        v-for="i in bot_list"
        class="my-2 flex h-fit border p-3 text-white"
        @mouseenter="i.hover = true"
        @mouseleave="i.hover = false"
      >
        <div class="flex min-h-full min-w-6 items-center justify-center">
          <div class="h-9 w-1 bg-gold transition-all"></div>
        </div>
        <div class="flex flex-col" >
          <div class="flex w-full items-center justify-between">
            <p class="text-black">{{ i.name }}</p>
            <img :src="'/imgs/' + i.icon + '-avatar.png'" class="w-[40px]" />
          </div>
          <p class="line-clamp-2" v-if="!i.hover">
            {{ i.desc }}
          </p>
          <p v-else>
            {{ i.desc }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
