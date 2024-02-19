<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
    <q-toolbar class="bg-primary text-white">
      <q-avatar >
      <img src="https://media.licdn.com/dms/image/D5603AQHrfmVRT8B_Jw/profile-displayphoto-shrink_200_200/0/1688958122279?e=2147483647&v=beta&t=qKpsYL3SlMZ2tTvj3m_2gnmyTeByGnvXZzl9LSrXxo0">
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
