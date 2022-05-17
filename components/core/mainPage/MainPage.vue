<template>
<div>
  <MainSection />
  <MedalSection />
</div>
</template>
<script>
import { defineComponent } from '@nuxtjs/composition-api';
import MainSection from './MainSection.vue';
import MedalSection from './MedalSection.vue';

export default defineComponent({
  components: {
    MainSection,
    MedalSection,
  },
});
</script>
