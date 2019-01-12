<template>
  <div class="row">
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 input-group mb-3">
        <div class="input-group-prepend">
          <span class="input-group-text">Quote</span>
        </div>
        <textarea class="form-control" rows="3" aria-label="Quote" v-model="quote"></textarea>
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quote: '',
    };
  },
  methods: {
    createNew() {
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    },
  },
};
</script>

<style>
  .btn {
    margin-left: 2em;
  }
</style>
