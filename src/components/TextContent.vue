<template>
  <div v-if="windowWidth > '800'" class="header">
    <img class="header__logo" src="../assets/images/logo.svg" alt="logo" />
  </div>
  <div class="text-content">
    <Headline />
    <p class="paragraph">
      Hello fellow shoppers! We're currently building our new fashion store. Add
      Add your email below to stay up-to-date with announcements and our deals.
      Email Address
    </p>
    <Form />
  </div>
</template>

<script>
import Headline from "@/components/Headline";
import Form from "@/components/Form";
import { useWindowSize } from "vue-window-size";

export default {
  name: "TextContent",
  components: {
    Headline,
    Form,
  },
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
@import "src/assets/globals.scss";

.header {
  position: absolute;
  top: 4rem;
  left: 0;
  width: 40%;
  height: auto;
  display: flex;
  justify-content: center;
}

.text-content {
  flex-grow: 3;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  @media (max-width: $breakpoint-smartphone) {
    padding-top: 4rem;
  }

  .paragraph {
    max-width: 25rem;
    padding: 1rem 4rem;
    text-align: left;
    line-height: 2rem;

    @media (max-width: $breakpoint-smartphone) {
      padding: 1rem 2rem;
      text-align: center;
    }
  }
}
</style>
