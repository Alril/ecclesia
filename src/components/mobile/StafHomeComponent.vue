<template>
  <div class="row justify-around">
    <q-card
      class="text-center"
      style="width: 110px"
      v-for="item in fitur"
      :key="item.title"
    >
      <q-avatar
        text-color="grey-8"
        icon="directions"
        class="q-ma-none q-pa-none"
      />
      <q-card-section class="text-center q-pa-none q-mt-sm">{{
        item.title
      }}</q-card-section>
    </q-card>
  </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup() {
    const fitur = [
      {
        title: "Jemaat",
        link: "",
      },
      {
        title: "Ibadah Raya",
        link: "",
      },
      {
        title: "Ibadah Tengah Minggu",
      },
    ];
    return {
      fitur,
    };
  },
};
</script>
