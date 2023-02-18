<template>
  <q-page padding class="flex flex-center">
    <q-card flat class="full-width q-pa-md">
      <img
        src="~assets/logo.png"
        style="width: 200px; height: 200px"
        fit="contain"
        class="q-mx-auto"
      />
      <q-form class="q-gutter-y-md">
        <q-input label="User Name" outlined v-model="user"></q-input>
        <q-input
          label="Password"
          outlined
          v-model="password"
          :type="visible ? 'text' : 'password'"
        >
          <template v-slot:append>
            <q-btn
              round
              :icon="visible ? 'fa-solid fa-eye-slash' : 'fa-solid fa-eye'"
              flat
              @click="visible = !visible"
            />
          </template>
        </q-input>
        <q-btn label="Submit" color="deep-orange" class="full-width q-py-md" />
      </q-form>
    </q-card>
  </q-page>
</template>

<script>
import { ref } from "vue";
export default {
  name: "LoginPage",
  setup() {
    const user = ref("");
    const password = ref("");
    const visible = ref(false);

    return {
      user,
      password,
      visible,
    };
  },
};
</script>
