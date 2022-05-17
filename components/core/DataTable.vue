<template>
  <v-data-table :headers="headers" :items="items" hide-default-footer>
   <slot v-for="(_, name) in $slots" :name="name" :slot="name"></slot>
    <template v-for="(_, name) in $scopedSlots" :slot="name" slot-scope="slotData">
      <slot :name="name" v-bind="slotData"></slot>
    </template>
  </v-data-table>
</template>
<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';

export default defineComponent({
  props: {
    headers: {
      type: Array,
      default: null,
    },
    items: {
      type: Array,
      default: null,
    },
  },
});
</script>
<style lang="scss">
    tr td {
      border: none !important;
    }
    tr:last-child {
      border-bottom:  1px solid #E9E9E9 !important;
      border-radius: 8px;
    }
    tbody {
      tr:nth-child(odd) {
        background-color: #F5F5F5;
      }
      border-left: 1px solid #E9E9E9;
      border-right: 1px solid #E9E9E9;
    }
    th span {
      justify-content: start;
      display: flex;
      align-self: center;
    }
    .v-data-table-header {
      border: 1px solid #E9E9E9;
      border-bottom: none;
      th {
        border-bottom: none !important;
      }
      border-radius: 8px !important;
    }
</style>
