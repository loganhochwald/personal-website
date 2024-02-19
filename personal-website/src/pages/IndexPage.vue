<template>
  <q-page class="top-left">
    <ResumeIcon />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import ResumeIcon from 'src/components/ResumeIcon.vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
    ResumeIcon,
  },
});
</script>

<style scoped>
.top-left {
  min-height: auto; /* or adjust as needed */
}
</style>
