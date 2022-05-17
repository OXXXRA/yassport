<template>
  <div class="mainSection">
    <div class="mainSection__cards">
      <div class="card--first">
      <MainCard />
      </div>
      <div class="card--second">
      <MainCard />
      </div>
      <div class="card--third">
      <MainCard />
      </div>
    </div>
    <div class="mainSection__titleBlock">
      <YassportRoundedLogo class="mainSection__titleBlock__logo" />
      <div class="mainSection__titleBlock__title">
        Your unique digital victories
      </div>
      <div class="mainSection__titleBlock__description">
        Save all awards and competition results<br> as digital NFT medals
      </div>
      <div class="mainSection__titleBlock__actions">
        <div class="mainSection__titleBlock__actions--register">
          <button @click="$router.push('/register')">Register</button>
        </div>
        <div class="mainSection__titleBlock__actions--explore">
          <button>
            <p>Explore</p>
            <ArrowIcon />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { defineComponent } from '@nuxtjs/composition-api'
import YassportRoundedLogo from '../../icons/YassportRoundedLogo.vue'
import ArrowIcon from '../../icons/ArrowIcon.vue'
import MainCard from './MainCard.vue';

export default defineComponent({
  components: {
    MainCard,
    YassportRoundedLogo,
    ArrowIcon,
  },
})
</script>
