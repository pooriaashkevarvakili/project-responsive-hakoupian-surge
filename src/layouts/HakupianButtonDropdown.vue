<template>
  <q-btn-dropdown
    icon="fa fa-user"
    class="text-left "
    color="primary"
    :label="$t('userPerson')"
  >
    <div  class="col">
      <div class="flex justify-center items-center">
        <div class="q-mt-xs q-ml-xs">
          <img src="image1.jpg" style="width=20px;height:50px" />
        </div>
        <div>
          <div class="q-mr-sm q-mt-xs ">{{ $t("Pooriavakili") }}</div>
          <div class="q-mr-sm q-mt-xs ">{{ $t("PortfolioView") }}</div>
        </div>
      </div>
    </div>
    <hr />
    <q-expansion-item
      v-for="item in hakupianButtonDropdown"
      :key="item.id"
      expand-icon="fa fa-chevron-left"
      expand-icon-class="text-blue-4"
      :icon="item.icon"
      size="6em"
      class="iran-sans text-blue-4"
     
      :label="item.label"
    >
    </q-expansion-item>
 
      <q-btn @click="gotoSignUp()" class="full-width bg-red-2">
     
        <q-item-label class="text-subtitle2 text-red-4 text-right iran-sans">{{
          $t("Signup")
        }}</q-item-label>
           <q-icon name="lock"></q-icon>
      </q-btn>
    
  </q-btn-dropdown>
</template>
<script>
import {useRouter} from "vue-router"
import { onMounted } from "vue";
import { useQuasar } from "quasar";
import { hakupianButtonDropdownCounter } from "stores/HakupianButtonDropdown";
export default {
  setup() {
    // const store = hakupianButtonDropdownCounter();
    // store.getHakupianButtonDropdown();
      const hakupianButtonDropdown=[
        {
      "id": 1,
      "label": "حضوروغیاب",
      "icon": "fa fa-dollar"
    },
    {
      "id": 2,
      "label": "حقوق مزایا",
      "icon": "fa fa-gift"
    },
    {
      "id": 3,
      "label": "خدمات",
      "icon": "fa fa-gift"
    },
    {
      "id": 4,
      "label": "ارزیابی",
      "icon": "fa fa-arrow-trend-up"
    },
    {
      "id": 5,
      "label": "آموزش",
      "icon": "fa fa-video"
    },
    {
      "id": 6,
      "label": "تنظیمات",
      "icon": "fa fa-gear"
    }
      ]
    const q = useQuasar();
    const router=useRouter()
   const gotoSignUp=()=>{
     router.push('/')
   }
    onMounted(() => {
      q.iconSet.arrow.dropdown = "";
    });
    return { 
      q, 
    // store,
  hakupianButtonDropdown,
    gotoSignUp };
  },
};
</script>

<style></style>
