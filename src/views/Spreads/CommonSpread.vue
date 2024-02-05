<script lang="ts" setup>
import TarotCard from "@/views/Components/TarotCard.vue";
import type { CardItem } from '@/views/Type';

withDefaults(
    defineProps<{
      cardSpread: CardItem[]
    }>(),
    {
      cardSpread: () => new Array().fill({}, 0, 6),
    }
)
</script>

<template>
  <div w-full flex="~ row gap-8 wrap" p8 flex-center>
    <div v-for="cardItem in cardSpread" style="width: 30%; height: 166px" flex-center>
      <div v-if="!cardItem.img"></div>
      <div v-else>
        <TarotCard is-back :card-info="cardItem" />
      </div>
    </div>
  </div>
</template>