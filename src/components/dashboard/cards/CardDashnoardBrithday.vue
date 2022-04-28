<template>
  <div class="col-md-3 col-lg-3 col-sm-12 col-xs-12">
    <q-card>
      <q-card-section >{{ $t("BrithdayDay") }}</q-card-section>
      <q-card-section v-for="item in Birthday" :key="item.id">
        <div class="flex">
          <q-avatar color="red-4" icon="fa fa-user"></q-avatar>
          <div class="flex-1">
            <div class=" text-subtitle2 q-mr-xs">
              {{ item.title }}
            </div>
            <div class=" text-subtitle2 q-mr-xs">
              {{ item.content }}
            </div>
          </div>
          <div >{{ item.date }}</div>
        </div>
      </q-card-section>
    </q-card>
  </div>
  <div></div>
</template>

<script>
import { birthdayCounter } from "stores/Birthday";
export default {
  setup() {
       const Birthday=[
         {
      "id":1,
      "title":"پوریاوکیلی",
      "content":"کارشناس نرم افزار",
      "date":"5بهمن" 
    },
    {
      "id":2,
      "title":"شهربازی",
      "content":"برنامه نویس",
      "date":"25خرداد"
    }
    ]
    // const store = birthdayCounter();
    // store.getBrithday();
    return { 
      // store
Birthday
       };
  },
};
</script>

<style></style>
