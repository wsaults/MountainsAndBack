<template>
  <div class="container">
      <div class="top"></div>
      <div class="bottom"></div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    .container {
        height: 4.4375rem;

        .top {
            background-color: $primary;
            height: 2.5rem;
        }

        .bottom {
            background-color: $secondary-darker;
            height: 0.5rem;
        }
    }
</style>
