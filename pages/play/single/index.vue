<script setup>
let bot_list = [
  {
    name: "Tit for tat",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "tit-for-tat",
  },
  {
    name: "Joss",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "joss",
  },
  {
    name: "Tit for two tat",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "tit-for-two-tat",
  },
  {
    name: "Suspicious",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "suspicious",
  },
  {
    name: "Pavlov",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "pavlov",
  },
  {
    name: "Grim trigger",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "grim-trigger",
  },
  {
    name: "AlwaysD",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "alwaysD",
  },
  {
    name: "AlwaysC",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "alwaysC",
  },
  {
    name: "Random",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "random",
  },
];
</script>
<template>
  <div class="bg_img_bot flex-center h-[100vh]">
    <DocumentInfo> some text </DocumentInfo>
    <div class="flex h-fit w-[clmap(300px,70%,900px)] flex-col border">
      <div
        v-for="i in bot_list"
        class="my-2 flex h-fit border text-white transition-all"
      >
        <div class="flex min-h-full min-w-6 items-center justify-center">
          <div class="size-4 bg-white"></div>
        </div>
        <div class="flex flex-col">
          <div class="flex w-full justify-between">
            <p>{{ i.name }}</p>
            <img :src="'/imgs/' + i.icon + '-avatar.png'" class="w-8" />
          </div>
          <p class="line-clamp-2 transition-all hover:line-clamp-none">
            {{ i.desc }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
