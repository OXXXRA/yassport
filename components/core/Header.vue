<template>
<div class="header" data-app>
  <div class="header__logo" @click="$router.push('/')">
    <YassportLogo />
  </div>
<div class="header__navigation">
  <div class="header__navigation__item">RESULTS</div>
  <div class="header__navigation__item">MEDALS</div>
</div>
<div class="header__login">
  <v-dialog v-model="loginDialog" width="400px">
    <template v-slot:activator="{ on }">
      <button v-on="on">
        <EnterIcon class="header__login__icon"/>
        <p class="header__login__text">Sign in</p>
      </button>
    </template>
      <div class="enter-form">
        <CloseIcon class="enter-form__close" @click="closeDialog"/>
        <div class="enter-form__title">Sign In</div>
        <input type="text" placeholder="Email" />
        <input type="text" placeholder="Password" />
        <button>Enter <ArrowIcon /></button>
        <div class="enter-form__footer">
          <p>Forgot password?</p>
          <span class="link">Register</span>
        </div>

      </div>
  </v-dialog>
</div>
</div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api';
import YassportLogo from '../icons/yassportLogo.vue';
import EnterIcon from '../icons/EnterIcon.vue';
import ArrowIcon from '../icons/ArrowIcon.vue';
import CloseIcon from '../icons/CloseIcon.vue';

export default defineComponent({
  components: {
    YassportLogo,
    EnterIcon,
    ArrowIcon,
    CloseIcon,
  },
  setup() {
    const loginDialog = ref<boolean>(false);
    const closeDialog = () => {
      console.log('11');
      loginDialog.value = false;
    };

    return {
      loginDialog,
      closeDialog
    }
  },
});
</script>
