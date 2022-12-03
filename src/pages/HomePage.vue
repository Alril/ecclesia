<template>
  <q-page>
    <div class="bg-orange-8" style="height: 420px; border-radius: 0 0 7em 7em">
      <q-toolbar>
        <q-toolbar-title class="text-center text-white text-bold text-h5"
          >GBI Ecclesia Manado</q-toolbar-title
        >
      </q-toolbar>
      <q-form class="q-pa-md">
        <q-input
          rounded
          outlined
          v-model="search"
          label="Search"
          bg-color="white"
        >
          <template v-slot:prepend>
            <q-icon name="search" />
          </template>
        </q-input>
      </q-form>
      <q-card class="q-mx-lg" style="border-radius: 1.5em">
        <q-toolbar>
          <q-toolbar-title class="text-center text-grey-8"
            >HUT Minggu ini</q-toolbar-title
          >
        </q-toolbar>
        <img src="https://cdn.quasar.dev/img/mountains.jpg" height="150" />
        <q-card-section>asdfasdfasdf</q-card-section>
      </q-card>
    </div>
    <staf-home />
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import StafHomeComponent from 'src/components/StafHomeComponent.vue';
export default defineComponent({
  // name: 'PageName'
  components: {
    StafHome: StafHomeComponent,
  },
  setup() {
    return {
      search: ref(''),
    };
  },
});
</script>
