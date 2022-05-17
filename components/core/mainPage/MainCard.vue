<template>
  <div class="mainSection__cards__cardWrapper">
    <div class="mainSection__cards__cardWrapper__image">
      <img :src="require('../../../static/medal1.png')" />
    </div>
    <InfoBlock />
  </div>
</template>
<script>
import { defineComponent } from '@nuxtjs/composition-api';
import InfoBlock from './InfoBlock.vue';

export default defineComponent({
  components: { InfoBlock },
});
</script>
