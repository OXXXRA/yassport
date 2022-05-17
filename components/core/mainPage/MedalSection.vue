<template>
  <div class="medalSection">
    <div class="medalSection__title">Medals</div>
    <div class="medalSection__medals">
      <div
        class="medalSection__medals__item"
        v-for="(item, index) in items"
        :key="index"
        :style="index > 3 ? 'margin-top: 70px' : ''"
      >
        <div class="medalSection__medals__item__image">
          <img :src="require('../../../static/medalSectionMedal1.png')" />
        </div>
        <div class="medalSection__medals__item__card">
          <MedalCard />
          <div class="medalSection__medals__item__card__footer">
            <div class="medalSection__medals__item__card__footer__favourite">
              <button>
                <img :src="require('../../../static/favourite.png')" />
              </button>
            </div>
            <div class="medalSection__medals__item__card__footer__see">
              <button @click="$router.push('medals/#2341')">
                See
                <LongArrowIcon />
              </button>
            </div>
          </div>
          <div class="medalSection__medals__item__card__title">
            <div class="medalSection__medals__item__card__title__id">#2341</div>
            <div class="medalSection__medals__item__card__title__text">
              RZD Golden Ring Ultra-Trail
              <div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="medalSection__loadMore">
      <button @click="items.push(1)">
        See more
      </button>
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from '@nuxtjs/composition-api';
import MedalCard from '../MedalCard.vue';
import LongArrowIcon from '../../icons/LongArrowIcon.vue'


export default defineComponent({
  components: {
    MedalCard,
    LongArrowIcon
  },
  setup() {
    const items = ref(new Array(8).fill('1'));
    return {
      items
    };
  },
})
</script>
