<template>
  <div class="container">
    <br />
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <br />
    <app-progress :size="currentSize"></app-progress>
    <app-quote-grid :quotes="quotes" @quoteDel="delQuote"></app-quote-grid>
    <br />
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on the quote to remove!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import ProgressBar from './components/Progress.vue';

export default {
  data() {
    return {
      quotes: [
        'This is a nice quote!',
        'Many many quotes',
      ],
      maxQuotes: 10,
    };
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appProgress: ProgressBar,
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes || quote.length < 1) {
        return;
      }
      this.quotes.push(quote);
    },
    delQuote(index) {
      this.quotes.splice(index, 1);
    },
  },
  computed: {
    currentSize() {
      return ((this.quotes.length / this.maxQuotes) * 100);
    },
  },
};
</script>

<style>

</style>
