<template>
  <div>
    <q-btn-dropdown
      menu-anchor="center left"
      icon-right="fa fa-plus"
      id="center"
      class="q-mt-xs circle text-black q-ml-xs"
    >
      <q-card style="max-width: 210px; width: 210px; height: 270px">
        <q-card-section dir="rtl">
          <q-input :label="$t('Search')" class="full-width input-six">
            <template v-slot:prepend>
              <q-icon name="search" />
            </template>
          </q-input>
          <div
            v-for="item in ButtonDropdownPage"
            :key="item.id"
            class="flex items-center q-mt-sm"
          >
            <img
              :src="item.img"
              style="width: 50px; height: 40px; border-radius: 50%"
            />

            <div class="q-mr-sm">{{ item.title }}</div>
          </div>
        </q-card-section>
      </q-card>
    </q-btn-dropdown>
  </div>
</template>

<script>
import { ButtonDropdownPageCounter } from "stores/ButtonDropdownPageButtonDropdownPage";
export default {
  setup() {
    const ButtonDropdownPage=[
      {
      "id":0,
      "title":"علیرضاتهرانی",
      "img":"https://s23.picofile.com/file/8449412092/image2.jpg"
    },
    {
      "id":1,
      "title":"پوریاوکیلی",
      "img":"https://s17.picofile.com/file/8419817268/image3.jpg"
    },
    {
      "id":2,
      "title":"محمددلیری",
      "img":"https://s23.picofile.com/file/8449412100/image4.png"
    },
    {
      "id":3,
      "title":"اشکان خورشیدی",
      "img":"https://s22.picofile.com/file/8449412126/image6.png"
    }
    ]
    // const store = ButtonDropdownPageCounter();
    // store.GetButtonDropdownPage();
    return {
      // store,
    ButtonDropdownPage
    };
  },
};
</script>

<style></style>
