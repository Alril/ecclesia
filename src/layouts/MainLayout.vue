<template>
  <q-layout view="lHh Lpr lFf">
    <q-footer>
      <q-tabs
        v-model="tab"
        indicator-color="transparent"
        active-color="deep-orange"
        class="bg-white text-grey-8 shadow-2"
        no-caps
      >
        <q-tab name="home" icon="home" label="Beranda" />
        <q-tab name="schedule" icon="schedule" label="Jadwal" />
        <q-tab name="birthday" icon="celebration" label="HUT" />
        <q-tab name="Profile" icon="manage_accounts" label="Profile" />
      </q-tabs>
    </q-footer>
    <q-page-container>
      <router-view class="bg-grey-2" />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  setup() {
    return {
      tab: ref("home"),
    };
  },
});
</script>
