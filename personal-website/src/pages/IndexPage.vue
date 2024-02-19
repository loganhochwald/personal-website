<template>
  <q-page class="bg-dark">
    <div class="q-pa-md">
    <div class="row">
      <div class="col">
        <ResumeIcon />
      </div>
    </div>
  </div>
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
