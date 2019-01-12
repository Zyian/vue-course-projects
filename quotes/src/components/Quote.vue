<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="card">
            <div class="card-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
};
</script>

<style>
  .card-body {
    font-family: Arizonia, cursive;
    font-size: 24px;
  }

  .card {
      margin-top: 2em;
  }

  .quote {
    cursor: pointer;
  }

  .quote:hover {
    background-color: rgb(250, 203, 203);
  }
</style>
