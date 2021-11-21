<template>
  <button class="button">{{ text }}</button>
</template>

<script>
export default {
  name: 'AppButton',
  props: {
    type: {
      type: String,
      default: 'button',
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
@import '../../styles/index';

.button {
  width: 100%;
  height: 30px;
  border: none;
  border-radius: 4px;
  background-color: $cerulean-light;
  color: #fffcee;
  font-weight: 500;
  font-family: 'Poppins', sans-serif;
  box-shadow: 0 4px 8px rgba(30, 60, 90, 0.2);
  transition: all 0.3s;
  justify-self: center;

  &:hover {
    filter: brightness(0.8);
  }
}

@media only screen and (min-width: $medium) {
  .button {
    width: 12.5rem;
    height: 40px;
    justify-self: end;
  }
}
</style>
