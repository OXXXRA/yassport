<template>
<div>
  <Header />
  <Nuxt />
  </div>
</template>

<script>
import { defineComponent } from '@nuxtjs/composition-api';
import Header from '../components/core/Header.vue';

export default defineComponent({
  components: {
    Header
  },
});
</script>
<style lang="scss">
@import url('../assets/main.scss');
</style>