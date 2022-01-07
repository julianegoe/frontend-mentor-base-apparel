<template>
  <section class="content">
    <slot />
  </section>
</template>

<script>
export default {
  name: "AppLayout",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "@/assets/globals.scss";

.content {
  margin: 0 auto;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-between;
  @media (max-width: $breakpoint-smartphone) {
    margin-top: 5rem;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
