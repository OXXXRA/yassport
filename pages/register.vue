<template>
  <div class="register">
    <div class="register__title">Register</div>
    <div class="register__content">
      <div class="register__content__form">
        <div class="register__content form__header">Name:</div>
        <div class="flex gap-6">
          <input type="text" class="form__input" placeholder="First name" />
          <input type="text" class="form__input" placeholder="Last name" />
        </div>
        <div class="flex mt-8 gap-7">
          <div class="flex flex-col">
            <div class="register__content form__header">Date of Birth:</div>
            <input type="text" class="form__input" placeholder="Last name" />
          </div>
          <div class="flex flex-col">
            <div class="register__content form__header">Gender:</div>
            <div class="flex gap-10">
              <div class="flex items-center gap-4">
                <input type="checkbox" class="form__input" />
                <p>Male</p>
              </div>
                <div class="flex items-center gap-4">
                <input type="checkbox" class="form__input" />
                <p>Female</p>
              </div>
            </div>
          </div>
        </div>
        <div class="register__content form__header mt-8">Contact</div>
        <input type="text" class="form__input" placeholder="@ Email" />

        <div class="register__content form__header mt-8">Password</div>
        <div class="flex gap-6">
          <input type="text" class="form__input" placeholder="Password" />
          <input type="text" class="form__input" placeholder="Password Confirmation" />
        </div>
        <div class="register__content__form__actions">
          <button>Register <ArrowIcon class="ml-4" /></button>
          <p>
            By signing up, you agree to Yassport<br>
            <span class="link">Privacy Policy</span> and <span class="link">Terms of Service</span>
          </p>
        </div>
        <div class="register__content__form__footer">
          <p>Already have an account?</p>
          <span>Sign in</span>
        </div>
      </div>
      <div class="register__content__logo">
        <BigYassportRoundedLogo />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';
import BigYassportRoundedLogo from '../components/icons/BigYassportRoundedLogo.vue';
import ArrowIcon from '../components/icons/ArrowIcon.vue';

export default defineComponent({
  components: { BigYassportRoundedLogo, ArrowIcon },
});
</script>
<style lang="scss">
.register {
  width: 100vw;
  height: 100vh;
  padding-left: 64px;
  padding-top: 59px;
  &__title {
    font-family: 'Poppins';
    font-style: normal;
    font-weight: 600;
    font-size: 32px;
    line-height: 48px;
    text-transform: uppercase;
    margin-bottom: 32px;
  }
  &__content {
    display: flex;
    &__form {
      padding: 32px;
      padding-bottom: 45px;
      background: #FFFFFF;
      border: 1px solid #E9E9E9;
      box-shadow: 0px 2px 4px rgba(200, 200, 200, 0.4);
      border-radius: 8px;
      width: 640px;
      .form__header {
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 24px;
        margin-bottom: 24px;
        }
      input[type=text].form__input {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding: 0px 16px;
        height: 52px;
        background: #F4F6F9;
        border: 1px solid #E9E9E9;
        border-radius: 4px;
      }
      &__actions {
        margin-top: 56px;
        display: flex;
        span.link {
          color: black;
          border-bottom: 1px solid #DDBE90;
        }
        p {
          font-family: 'Poppins';
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 24px;
          color: #6D7580;
          margin-left: 16px;
        }
        button {
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 16px 24px;
          width: 185px;
          height: 52px;
          background: #DDBE90;
          border-radius: 4px;
        }  
      }
      &__footer { 
        span {
          margin-left: 16px;
          color: #DDBE90;
        }
        margin-top: 34px;
        padding-top: 43px;
        border-top: 1px solid #E9E9E9;
        display: flex;
        font-family: 'Poppins';
        font-weight: 500;
        font-size: 16px;
        line-height: 24px;
        align-items: center;
        justify-content: center;
        color: #000000;
      }
    }
    &__logo {
      margin-top: auto;
      margin-bottom: auto;
      margin-left: 200px;
    }
  }
}
</style>