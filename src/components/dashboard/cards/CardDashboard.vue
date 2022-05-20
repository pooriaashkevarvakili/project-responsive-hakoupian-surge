<template>
  <div class="row q-col-gutter-sm q-py-sm">
    <div v-for="(item, index) in cardDashboard" :key="index" class="col-md-3 col-lg-3 col-sm-12 col-xs-12">
      <q-card>
        <q-card-section class="row">
          <div class="col">
            <div class="flex">
              <div>
                <q-avatar :color="item.color" :class="item.colorIcon" :icon="item.icon"></q-avatar>
              </div>
              <div>
                <div class="q-mr-sm q-mt-xs">{{ item.title }}</div>
                <div class="q-mr-sm q-mt-xs">{{ item.content }}</div>
              </div>
            </div>
          </div>
        </q-card-section>
      </q-card>
    </div>
  </div>

  <CardDashboardOne />
</template>

<script setup>
import { CardDashboardCounter } from "stores/CardDashboard";
import CardDashboardOne from "./CardDashboardOne.vue"
const cardDashboard = [
  {
    "title": "امروز چهارشنبه",
    "content": "25اسفند",
    "color": "red-3",
    "icon": "fa fa-calendar",
    "colorIcon": "text-red-4"
  },
  {
    "title": "ساعت ورود",
    "content": "7:55",
    "color": "blue-3",
    "icon": "alarm",
    "colorIcon": "text-blue-4"

  },
  {
    "title": "مانده مرخصی",
    "content": "7روز",
    "color": "red-3",
    "icon": "fa fa-bell",
    "colorIcon": "text-orange-4"
  },
  {
    "title": "درصدپیشرفت تسک ها",
    "content": "75درصد",
    "color": "green-3",
    "icon": "fa fa-chart-simple",
    "colorIcon": "text-green-6"
  }
]
    // const store = CardDashboardCounter();
    // store.getPosts();
</script>
<style>
</style>
