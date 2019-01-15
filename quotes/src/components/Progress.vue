<template>
  <div class="row">
    <div class="col-sm-12">
      <div class="progress">
        <div class="progress-bar" role="progressbar" :style="progStyle"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['size'],
  computed: {
    progStyle() {
      return {
        width: `${this.size}%`,
      };
    },
  },
};
</script>

<style>

</style>
