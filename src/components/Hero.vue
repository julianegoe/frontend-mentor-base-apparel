<template>
  <div v-if="windowWidth > '1100'" class="hero">
    <img src="../assets/images/hero-desktop.jpg" class="desktop" />
  </div>
  <div v-if="windowWidth <= '1100'" class="hero">
    <img src="../assets/images/hero-mobile.jpg" class="smartphone" />
  </div>
</template>

<script>
import { useWindowSize } from "vue-window-size";

export default {
  name: "Hero",
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

.hero {
  object-fit: cover;
}

</style>
