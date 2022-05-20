<template>
  <div class="row q-col-gutter-sm q-py-sm">
    <CardDashboardTwo />
    <div class="col-md-3 col-lg-3 col-sm-12 col-xs-12">
      <q-card>
        <q-card-section>{{ $t("Recentworks") }}</q-card-section>
        <q-card-section v-for="item in Recentworks" :key="item.id">
          <div class="flex">
            <q-icon name="more_vert" :class="item.color" style="font-size: 1.8em"></q-icon>
            <div class="flex-1">
              <div>{{ item.title }}</div>
              <div>{{ item.content }}</div>
            </div>
            <div>{{ item.date }}</div>
          </div>
        </q-card-section>
        <q-card-section>
          <q-btn icon="fa fa-chevron-right" class="full-width bg-blue-4 text-white">{{ $t("ShowWorks") }}</q-btn>
        </q-card-section>
      </q-card>
    </div>
    <CardDashboardLatestNotification />
    <CardDashboardBrithday />
  </div>
</template>
<script setup>
import { RecentworksCounter } from "stores/Recentworks";
import CardDashboardTwo from "components/dashboard/cards/CardDashboardTwo.vue"
import CardDashboardBrithday from "components/dashboard/cards/CardDashnoardBrithday.vue"
import CardDashboardLatestNotification from "components/dashboard/cards/CardDashboardLatestNotification.vue"
// const store = RecentworksCounter();
// store.getRecentworks();
const Recentworks = [
  {
    "id": 1,
    "title": "دیزاین صفحه داشبوردهاکوپیان360",
    "content": "از طرف سعید رحیمی",
    "color": "blue-2",
    "date": "5خرداد98"
  },
  {

    "id": 2,
    "title": "تحقیق درمورد بخش میزکار",
    "content": "ازطرف حسین وفایی",
    "date": "2خرداد98",
    "color": "text-red-5"
  },
  {
    "id": 3,
    "title": "دیزاین صفحات بخش جذب واستخدام",
    "content": "ایجادشده توسط حسین مجیدی",
    "date": "1خرداد",
    "color": "text-green-5"
  },
  {
    "id": 4,
    "title": "دیزاین صفحه لاگین وثبت نام",
    "content": "از طرف سعید رحیمی",
    "date": "28اردیبهشت98",
    "color": "text-orange-4"
  }
]
</script>
<style>
</style>
