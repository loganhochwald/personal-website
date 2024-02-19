<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
    <q-toolbar class="bg-primary text-white">
      <q-avatar >
      <img src="https://cdn.quasar.dev/img/avatar.png">
    </q-avatar>

      <q-toolbar-title>Logan Hochwald</q-toolbar-title>

      <div>{{ time }}</div>
      <q-btn dense flat icon="battery_charging_full" />
      <q-btn dense flat icon="wifi" />
    </q-toolbar>
  </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup() {
    const time = ref('');

    setInterval(() => {
      const currentTime = new Date();
      const formattedTime = currentTime.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
      time.value = formattedTime;
    }, 1000);

    return { time };
  },
});
</script>
