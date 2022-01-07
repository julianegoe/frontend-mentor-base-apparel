<template>
  <form class="form">
    <input
      class="form__input"
      type="text"
      id="email"
      name="email"
      placeholder="Email Address"
    />
    <button class="form__button">
      <img src="../assets/images/icon-arrow.svg" alt="arrow" />
    </button>
  </form>
</template>

<script>
export default {
  name: "Form",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "src/assets/globals.scss";

.form {
  display: flex;
  position: relative;
  left: 2rem;
  justify-content: center;
  padding-top: 1rem;
  &__input {
    width: 100%;
    color: $color-desaturated-red;
    font-weight: $font-weight-semibold;
    border: 1px solid $color-desaturated-red;
    border-radius: 999px;
    padding: 1rem 5rem 1rem 1rem;
  }
}

.form__button {
  width: 8rem;
  height: auto;
  padding: 1rem 0 1rem 0;
  border: none;
  background-image: $gradient-2;
  border-radius: 999px;
  cursor: pointer;
  position: relative;
  right: 4rem;
  z-index: 100;
}

::placeholder {
  color: $color-desaturated-red;
  font-weight: $font-weight-semibold;
  opacity: 0.5;
}
</style>
