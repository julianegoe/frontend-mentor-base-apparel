<template>
  <Header />
  <app-layout>
    <Hero />
    <TextContent />
  </app-layout>
</template>

<script>
import Header from "@/components/Header.vue";
import AppLayout from "@/layouts/AppLayout.vue";
import Hero from "@/components/Hero";
import TextContent from "@/components/TextContent";

export default {
  name: "App",
  components: { TextContent, Hero, Header, AppLayout },
};
</script>

<style lang="scss">
@import "@/assets/globals.scss";

body {
  background-image: $gradient-1;
}

</style>
