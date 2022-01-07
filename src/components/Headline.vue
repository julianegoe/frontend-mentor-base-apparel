<template>
  <div class="headline">
    <h1 class="headline__top">We're</h1>
    <h1 class="headline__bottom">Coming</h1>
    <h1 class="headline__bottom">Soon</h1>
  </div>
</template>

<script>
export default {
  name: "Headline",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "@/assets/globals.scss";

.headline {
  text-align: left;

  @media (max-width: $breakpoint-smartphone) {
    text-align: center;
  }

  &__top {
    color: $color-desaturated-red;
    font-weight: $font-weight-light;
  }

  &__bottom {
    color: $color-dark-greyish-red;
    font-weight: $font-weight-semibold;
  }
}
</style>
