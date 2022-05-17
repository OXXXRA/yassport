<template>
        <div class="my-profile__content__info">
        <div class="my-profile__content__info__title">About</div>
        <div class="flex gap-6">
          <div class="form-item">
            <div class="my-profile__content__info__header">Name</div>
            <input type="text" class="input--dense" />
          </div>
          <div class="form-item">
            <div class="my-profile__content__info__header">Last name</div>
            <input type="text" class="input--dense" />
          </div>
        </div>
        <div class="flex gap-6 mt-6">
          <div class="form-item">
            <div class="my-profile__content__info__header">Gender</div>
            <input type="text" class="input--dense" />
          </div>
          <div class="form-item">
            <div class="my-profile__content__info__header">Birth</div>
            <input type="text" class="input--dense" />
          </div>
        </div>
        <div class="my-profile__content__info__title">Contacts</div>
        <div class="form-item">
          <div class="my-profile__content__info__header">Email</div>
          <input type="text" class="input--dense small" />
        </div>
        <div class="my-profile__content__info__actions">
          <button>Request to change<ArrowIcon /></button>
          <p>Send us a request to change<br />your personal information</p>
        </div>
      </div>
</template>
<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import ArrowIcon from '../../icons/ArrowIcon.vue'

export default defineComponent({
  components: { ArrowIcon },
})
</script>