<template>
  <div v-if="windowWidth <= '1100'" class="header">
    <img class="header__logo" src="../assets/images/logo.svg" alt="logo" />
  </div>
</template>

<script>
import { useWindowSize } from "vue-window-size";

export default {
  name: "Header",
  components: {},
  setup() {
    const { width, height } = useWindowSize();
    return {
      windowWidth: width,
      windowHeight: height,
    };
  },
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
