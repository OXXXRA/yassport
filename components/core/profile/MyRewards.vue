<template>
  <div class="my-rewards">
    <div class="my-rewards__info">
      <div class="my-rewards__info__title">
        SPB Half Marathon "Northern Capital"
      </div>
      <MedalCard />
      <div class="my-rewards__info__results">
        <div class="flex gap-8">
          <div class="my-rewards__info__results__item">
            <div class="flex">
              <div class="my-rewards__info__results__item__icon">
                <span>⏱</span>
              </div>
              <div class="flex-col">
                <div class="my-rewards__info__results__item__header">
                  Start number:
                </div>
                <div class="my-rewards__info__results__item__value">#4324</div>
              </div>
            </div>
          </div>
          <div class="my-rewards__info__results__item">
            <div class="flex">
              <div class="my-rewards__info__results__item__icon">
                <span>🏆</span>
              </div>
              <div class="flex-col">
                <div class="my-rewards__info__results__item__header">
                  Result:
                </div>
                <div class="my-rewards__info__results__item__value">
                  32 : 15
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="my-rewards__info__results__item mt-6">
          <div class="flex">
            <div class="my-rewards__info__results__item__icon">
              <span>🎖</span>
            </div>
            <div class="flex-col">
              <div class="my-rewards__info__results__item__header">Place:</div>
              <div class="my-rewards__info__results__item__value">#1</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="my-rewards__medal">
      <img :src="require('../../../static/BigAccMedal.png')" />
      <button>See result <AccountArrowIcon /></button>
    </div>
  </div>
</template>
<script>
import { defineComponent } from '@nuxtjs/composition-api'
import MedalCard from '@/components/core/MedalCard.vue'
import AccountArrowIcon from '@/components/icons/AccountArrowIcon.vue';

export default defineComponent({
  components: { MedalCard, AccountArrowIcon },
})
</script>
<style lang="scss">
.my-rewards {
  display: flex;
  gap: 24px;
  &__medal {
    button {
      margin-top: 24px;
      box-sizing: border-box;
      display: flex;
      align-items: center;
      padding: 16px;
      gap: 48px;
      width: 421px;
      height: 52px;
      background: #DDBE90;
      border: 1px solid #DDBE90;
      border-radius: 4px;
      font-family: 'Poppins';
      font-weight: 400;
      font-size: 18px;
      line-height: 20px;
    }
  }
  &__info {
    width: 533px;
    height: 520px;
    padding: 32px;
    background: #ffffff;
    border: 1px solid #e9e9e9;
    box-shadow: 0px 2px 4px rgba(200, 200, 200, 0.4);
    border-radius: 8px;
    &__title {
      font-family: 'Poppins';
      font-weight: 600;
      font-size: 20px;
      color: #1e1e1e;
      margin-bottom: 48px;
    }
    &__results {
      margin-top: 48px;
      &__item {
        &__header {
          font-family: 'Poppins';
          font-weight: 400;
          font-size: 20px;
          color: #818181;
          margin-bottom: 8px;
        }
        &__value {
          font-family: 'Poppins';
          font-weight: 400;
          font-size: 18px;
          line-height: 30px;
          color: #1e1e1e;
        }
        &__icon {
          margin-right: 8px;
          display: flex;
          width: 48px;
          height: 48px;
          font-size: 20px;
          border: 1px solid #e9e9e9;
          border-radius: 200px;
          justify-content: center;
          span {
            align-self: center;
          }
        }
      }
    }
  }
  .medalSection__medals__item__card__body {
    margin-top: 48px;
    padding-top: 26px;
    padding-left: 27px;
    margin-bottom: 48px;
    padding-bottom: 32px;
    box-shadow: none;
    padding-right: 140px;
    background: #ffffff;
    border: 1px solid #e9e9e9;
    border-radius: 8px;
    &__infoBlock {
      width: 140px;
      &__header {
        align-items: center;
        font-size: 20px;
        & > svg {
          width: 18px;
          height: 20px;
        }
      }
      &__value {
        font-size: 18px;
      }
    }
  }
}
</style>
