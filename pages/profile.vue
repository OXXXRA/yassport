<template>
  <div class="my-profile">
    <div class="my-profile__title">Your Account</div>
    <div class="my-profile__content">
      <div class="sidebar flex flex-col">
        <div class="my-profile__content__tabs">
          <div @click="currentTab = 1" :class="[currentTab === 1 ? 'tab--active' : '' , 'my-profile__content__tabs__tab']">Rewards</div>
          <div @click="currentTab = 2" :class="[ currentTab === 2 ? 'tab--active' : '' , 'my-profile__content__tabs__tab']">
            Personal information
          </div>
        </div>
        <button class="my-profile__content__question">Ask a question</button>
      </div>
      <keep-alive>
      <component :is="getComponentFromTab" />
      </keep-alive>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref, computed } from '@nuxtjs/composition-api'
import AccountInformation from '@/components/core/profile/AccountInformation.vue';
import MyRewards from '@/components/core/profile/MyRewards.vue';


export default defineComponent({
 components: {
    AccountInformation,
    MyRewards
 },
 setup() {
   const currentTab = ref<number>(0);
   const listComponents:Record<number, string> = {
      1: 'MyRewards',
      2: 'AccountInformation',
   };
   const getComponentFromTab = computed(():string => listComponents[currentTab.value]);
   return {
     currentTab,
     getComponentFromTab
   }
 },
});
</script>
