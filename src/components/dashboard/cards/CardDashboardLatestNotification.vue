<template>
  <div dir="rtl" class="col-md-3 col-lg-3 col-sm-12 col-xs-12">
    <q-card>
      <q-card-section>{{ $t("LatestNotifications") }}</q-card-section>
      <q-card-section v-for="item in Latestnotifications" :key="item.id">
        <div :key="item.id" class="flex">
          <q-avatar
            :class="item.colorIcon"
            :color="item.color"
            :icon="item.icon"
          ></q-avatar>
          <div class="flex-1">
            <div class="q-mr-xs">{{ item.title }}</div>
            <div class="q-mr-xs">{{ item.content }}</div>
          </div>
        </div>
      </q-card-section>
      <q-card-section>
        <q-btn
          icon="fa fa-chevron-right"
          class="full-width iran-sans text-white bg-blue-4"
          >{{ $t("SeeAll") }}</q-btn
        >
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import { LatestnotificationsCounter } from "stores/Latestnotifications";
export default {
  setup() {
    // const store = LatestnotificationsCounter();
    // store.getlatestnotifications();
 const Latestnotifications=[
   {
      "id":1,
      "title":"شما سه تماس از دست رفته دارید",
      "content":"2روزقبل",
      "icon":"fa fa-phone",
      "color":"red-2",
      "colorIcon":"text-red-4"
    },
    
    {
      "id": 2,
      "title": "درخواست مرخصی شما تایید شد",
      "content": "1روزقبل",
      "icon": "fa fa-calendar",
      "color": "green-4",
      "colorIcon":"text-green-6"
    },
    {
      "id": 3,
      "title": "یاداوری جلسه منابع انسانی",
      "content": "20خرداد98",
      "icon": "fa fa-bell",
      "color": "blue-4",
      "colorIcon":"text-blue-2"
    },
    {
      "id": 4,
      "title": "شما2ایمیل جدیددارید",
      "content": "20خرداد98",
      "icon": "mail",
      "color": "red-4",
      "colorIcon":"text-blue-2"
    }
 ]
   
    return {
      // store,
      Latestnotifications
    };
  },
};
</script>

<style></style>
