<template>
<MainPage />
</template>

<script lang="ts">
import MainPage from '../components/core/mainPage/MainPage.vue';
import { defineComponent } from '@nuxtjs/composition-api';

export default defineComponent({
  components: {
    MainPage
  },
});
</script>
