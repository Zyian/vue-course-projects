<template>
  <div class="row">
    <app-quote v-for="(q,i) in quotes" :key="i" @click.native="deleteQuote(i)">{{ q }}</app-quote>
  </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
  props: ['quotes'],
  components: {
    appQuote: Quote,
  },
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDel', index);
    },
  },
};
</script>

<style>
</style>
