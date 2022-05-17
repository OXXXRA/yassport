<template>
  <div class="medalSection__medals__item__card__body">
    <div class="row">
      <div class="medalSection__medals__item__card__body__infoBlock">
        <div class="medalSection__medals__item__card__body__infoBlock__header">
          <CalendarIcon /> Year:
        </div>
        <div class="medalSection__medals__item__card__body__infoBlock__value">
          2022
        </div>
      </div>
      <div class="medalSection__medals__item__card__body__infoBlock">
        <div class="medalSection__medals__item__card__body__infoBlock__header">
          <LightningIcon /> Distance:
        </div>
        <div class="medalSection__medals__item__card__body__infoBlock__value">
          42.2 km
        </div>
      </div>
    </div>
    <div class="row">
      <div class="medalSection__medals__item__card__body__infoBlock">
        <div class="medalSection__medals__item__card__body__infoBlock__header">
          <LocationIcon /> Location:
        </div>
        <div class="medalSection__medals__item__card__body__infoBlock__value">
          Russia - Kazan
        </div>
      </div>
      <div class="medalSection__medals__item__card__body__infoBlock">
        <div class="medalSection__medals__item__card__body__infoBlock__header">
          <FinishIcon /> Type:
        </div>
        <div class="medalSection__medals__item__card__body__infoBlock__value">
          Running 👟
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'
import FinishIcon from '../icons/FinishIcon.vue'
import CalendarIcon from '../icons/CalendarIcon.vue'
import LightningIcon from '../icons/LightningIcon.vue'
import LocationIcon from '../icons/LocationIcon.vue'

export default defineComponent({
  components: {
    FinishIcon,
    CalendarIcon,
    LightningIcon,
    LocationIcon,
  },
})
</script>

