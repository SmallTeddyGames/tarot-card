<script lang="ts" setup>
import CommonSpread from "@/views/Spreads/CommonSpread.vue";
import type { CardItem } from '@/views/Type';

const commonCardSpread: Ref<CardItem[]> = ref([
  { type: '', content: '', img: ''},
  { type: 'sun', content: 'sun', img: 'sun.png' },
  { type: '', content: '', img: ''},
  { type: 'sun', content: 'sun', img: 'sun.png' },
  { type: 'sun', content: 'sun', img: 'sun.png' },
  { type: 'sun', content: 'sun', img: 'sun.png' }
])
</script>

<template>
  <div h-full w-screen color-white p8 flex gap-8>
    <div h-full w-full of-hidden flex-center border="1px dashed #666" border-rd-2 bg-mask>卡牌区域</div>
    <div h-full w-full of-hidden flex-center border="1px dashed #666" border-rd-2 bg-mask>
      <CommonSpread :card-spread="commonCardSpread" />
    </div>
  </div>
</template>
