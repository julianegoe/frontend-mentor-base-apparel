<template>
  <div class="header">
    <img class="header__logo" src="../assets/images/logo.svg" alt="logo" />
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "@/assets/globals.scss";

.header {
  position: absolute;
  top: 0;
  left: 0;
  width: 50%;
  height: auto;

  @media (max-width: $breakpoint-smartphone) {
    background-color: white;
  }
  .header__logo {
    padding: 1rem;
  }
}
</style>
