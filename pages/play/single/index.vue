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
onMounted(() => {
  let el = document.querySelectorAll("#card");
  el.forEach((x) => {
    x.addEventListener("mouseenter", () => {
      x.classList.toggle("card-animation");
    });
  });
  el.forEach((x) => {
    x.addEventListener("mouseleave", () => {
      x.classList.toggle("card-animation");
    });
  });
});
</script>
<template>
  <div class="bg_img_bot h-[100vh] overflow-y-scroll py-10">
    <DocumentInfo> some text </DocumentInfo>
    <div
      class="mx-auto flex h-fit w-[clamp(300px,70%,900px)] flex-col transition-all hover:max-h-[300px]"
    >
      <div
        id="card"
        v-for="i in bot_list"
        class="my-2 flex h-fit border p-3 text-white"
      >
        <div class="flex min-h-full min-w-6 items-center justify-center">
          <div class="bg-gold h-9 w-1"></div>
        </div>
        <div class="flex flex-col">
          <div class="flex w-full items-center justify-between">
            <p class="text-black">{{ i.name }}</p>
            <img :src="'/imgs/' + i.icon + '-avatar.png'" class="w-[40px]" />
          </div>
          <p class="line-clamp-2">
            {{ i.desc }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
