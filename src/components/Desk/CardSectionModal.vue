<template>
  <q-card-section>
    <div class="flex items-center justify-center">
      <img src="image1.jpg" style="width:60px;height:60px;border-radius:50%,overflow:hidden" />
      <div class="flex-1">
        <div class="q-mr-xs">علیرضاتهرانی</div>
        <div class="q-mr-xs">{{ $t('Salaryincrease') }}</div>
        <div class="q-mr-xs">{{ $t('Summoningyou') }}</div>
      </div>
      <div class="q-mr-xs">13:58</div>
    </div>
    <div v-for="item in CardSectionModal" :key="item.id" class="flex q-mt-lg items-center justify-center">
      <img :src="item.img" style="width: 60px; height: 60px; border-radius: 50%; overflow: hidden" />
      <div class="flex-1">
        <div class="q-mr-xs">{{ item.title }}</div>
        <div class="q-mr-xs">{{ $t('Salaryincrease') }}</div>
        <div class="q-mr-xs">{{ item.content }}</div>
      </div>
      <div class="q-mr-xs">{{ item.date }}</div>
    </div>
  </q-card-section>
</template>
<script setup>
import { CardSectionModalCounter } from "stores/CardSectionModal";
const CardSectionModal = [
  {
    "id": 1,
    "title": "پوریا وکیلی",
    "img": "https://s23.picofile.com/file/8449412134/image7.png",
    "date": "13:58",
    "content": "با سلام به استیحضار می رسانم"
  },
  {
    "id": 2,
    "title": "محمددلیری",
    "img": "https://s23.picofile.com/file/8449412092/image2.jpg",
    "date": "8:01",
    "content": "با سلام به استیحضار می رسانم"
  },
  {
    "id": 3,
    "title": "حسین صادقی",
    "img": "https://s17.picofile.com/file/8419817268/image3.jpg",
    "date": "14:01",
    "content": "با سلام به استیحضار می رسانم"
  },
  {
    "id": 4,
    "title": "ابراهیم صادقی",
    "img": "https://s23.picofile.com/file/8449412100/image4.png",
    "date": "14:01",
    "content": "با سلام به استیحضار می رسانم"
  },
  {
    "id": 5,
    "title": "وحید شکاری",
    "img": "https://s23.picofile.com/file/8449412118/image5.png",
    "date": "15:01",
    "content": "با سلام به استیحضار می رسانم"
  },
  {
    "id": 6,
    "title": "زینب امیری",
    "img": "https://s22.picofile.com/file/8449412126/image6.png",
    "date": "10:01",
    "content": "با سلام به استیحضار می رسانم"
  }
]
    // const store = CardSectionModalCounter();
    // store.GetCardSectionModal();
</script>
<style>
</style>
