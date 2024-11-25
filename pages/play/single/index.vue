<script setup lang="ts">
let botList = ref([
  {
    name: "Tit For Tat",
    desc: "This widely recognized strategy, championed by Robert Axelrod in game theory tournaments, prioritizes cooperation but retaliates against betrayal. It starts with cooperation, then mimics the opponent's action in subsequent rounds. This fosters cooperation if both players prioritize long-term benefits. It can represent a fair and adaptable AI in your game.",
    icon: "tit-for-tat",
  },
  {
    name: "Joss",
    desc: "Essentially, Joss is a more suspicious version of Tit-for-Tat. It starts by cooperating but is quick to defect if it perceives the opponent as being too cooperative. This strategy can be effective in environments where there are many players using deceptive strategies, as it can quickly identify and punish them.",
    icon: "joss",
  },
  {
    name: "Tit For Two Tat",
    desc: " This cautious variant of TFT adds a layer of forgiveness. It cooperates first, then cooperates again if the opponent cooperated, but defects twice if the opponent initially defects. This strategy offers a second chance for cooperation but punishes repeated betrayals more severely than TFT.  It can represent an AI that values cooperation but prioritizes protecting itself from exploitation.",
    icon: "tit-for-two-tat",
  },
  {
    name: "Suspicious",
    desc: "This strategy reflects a cynical outlook. Similar to TFT, it cooperates initially, but assumes the opponent will defect. It only cooperates in the first round if the opponent cooperates. This approach can be effective against populations with a high prevalence of AlwaysD bots, but might miss opportunities for cooperation with more trustworthy strategies.",
    icon: "suspicious",
  },
  {
    name: "Pavlov",
    desc: "This algorithm draws inspiration from classical conditioning. It starts with cooperation. If the opponent defects, it defects in the next round. However, if the opponent cooperates and it gets rewarded, it keeps cooperating with a small chance of randomly defecting. This strategy encourages cooperation through positive reinforcement but maintains some unpredictability. It can represent an AI that learns from past interactions but retains a degree of cautiousness.",
    icon: "pavlov",
  },
  {
    name: "Grim Trigger",
    desc: "This unforgiving strategy embodies the saying 'once bitten, twice shy.' It starts with cooperation, extending an olive branch, but defects permanently after the first betrayal by the opponent. This discourages defection as the opponent risks losing a future cooperator. It can be a good choice against populations with many AlwaysD bots, but might struggle against more forgiving strategies.",
    icon: "grim-trigger",
  },
  {
    name: "AlwaysD",
    desc: "This antagonist prioritizes personal gain, always defecting to secure the higher immediate payoff. While effective against trusting bots, it can lead to mutually negative outcomes if both players employ this strategy. It can represent a selfish or short-sighted AI in your game.",
    icon: "alwaysD",
  },
  {
    name: "AlwaysC",
    desc: "This guileless bot epitomizes trust, consistently cooperating regardless of the opponent's actions. While noble, it can be easily exploited by more ruthless strategies. It might be suitable for introductory levels or to encourage cooperation in early stages of the game.",
    icon: "alwaysC",
  },
  {
    name: "Random",
    desc: "This unpredictable bot injects chaos into the game. It randomly chooses between cooperating and defecting each round. This can be a good way to model real-world scenarios where decisions might be influenced by external factors or uncertainty. It can make the game more challenging and unpredictable for the player.",
    icon: "random",
  },
]);
let hoverEl = ref();
</script>
<template>
  <div class="img-bot-selection h-[100vh] overflow-y-scroll py-10">
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
        v-for="i in botList"
        class="my-2 flex h-fit border p-3 text-white transition-all duration-500"
        @mouseenter="hoverEl = i"
        @mouseleave="hoverEl = undefined"
        :class="{ 'bg-yellow-300 !text-black ': hoverEl === i }"
      >
        <div class="flex min-h-full min-w-6 items-center justify-center">
          <div class="bg-gold h-9 w-1 transition-all"></div>
        </div>
        <div class="flex flex-col">
          <div class="flex w-full items-center justify-between">
            <p class="text-black">{{ i.name }}</p>
            <img :src="'/imgs/' + i.icon + '-avatar.png'" class="w-[40px]" />
          </div>
          <Transition name="bounce">
            <p v-if="hoverEl === i" class="appear-animation">
              {{ i.desc }}
            </p>
            <p v-else class="line-clamp-2">
              {{ i.desc }}
            </p>
          </Transition>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.bounce-enter-active {
  @apply transition-all duration-500;
}
.bounce-enter-from {
  @apply opacity-0;
}
.bounce-leave-to {
  @apply opacity-100;
}
</style>
