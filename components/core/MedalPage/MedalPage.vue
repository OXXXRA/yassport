<template>
  <div>
    <div class="medalPage__return"><ShortArrowIcon /> Go back</div>
    <div class="medalPage__medalBlock">
      <div class="medalPage__medalBlock__album">
        <img class="medalPage__medalBlock__album__main" :src="require('../../../static/medal1.png')" />
        <div class="medalPage__medalBlock__album__wrapper">
           <img :src="require('../../../static/medal1.png')" v-for="i in 3" :key="i"/>
        </div>
      </div>
      <div class="medalPage__medalBlock__info">
        <div class="medalPage__medalBlock__info__id">#2341</div>
        <div class="medalPage__medalBlock__info__title">
          RZD Golden Ring Ultra-Trail
        </div>
        <div class="medalPage__medalBlock__info__about">
          <div class="text--subtitle">About:</div>
          <p>
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book. It has survived not
            only five centuries, but also the leap into electronic typesetting,
            remaining essentially unchanged.
          </p>
        </div>
        <MedalCard />
        <div class="medalPage__medalBlock__info__actions">
          <button>Add result</button>
          <p>To add medal in your list of rewards, you should<br>
            <a>register</a> first.
          </p>
        </div>
      </div>
    </div>
    <div class="medalPage__results">
      <div class="medalPage__results__title">Results</div>
      <div class="medalPage__results__search">
        <input type="text" placeholder="Search via name or start number"/>
      </div>
      <data-table :headers="headers" :items="testValues" hide-default-footer>
        <template v-slot:[`item.actions`]="">
          <NuxtLink to="/">More</NuxtLink>
        </template>
      </data-table>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api';
import MedalCard from '../MedalCard.vue';
import DataTable from '../DataTable.vue';

export default defineComponent({
  components: {
    MedalCard,
    DataTable,
  },
  setup() {
    const headers = ref([
      { text: '🎖 Place', value: 'place', sortable: false },
      { text: '⏱ Start number', value: 'startNumber', sortable: false },
      { text: '👦 Name', value: 'name', sortable: false },
      { text: '🏆 Result', value: 'result', sortable: false },
      { text: '', value: 'actions', sortable: false },
    ]);

    const testValues = ref([
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
      { place: '🥇 1', startNumber: '#4324', name: 'Anatoliy Mitroshin', result: '32 : 15' },
    ]);

    return {
      headers,
      testValues
    };
  },
})
</script>
