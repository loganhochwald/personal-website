<template>
  <q-page class="flex flex-center">
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
