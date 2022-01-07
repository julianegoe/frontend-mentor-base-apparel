<template>
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

export default {
  name: "TextContent",
  components: {
    Headline,
    Form,
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/globals.scss";

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
