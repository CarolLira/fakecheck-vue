<template>
  <section class="description">
    <h1 class="description__message">
      Você pode checar se a sua notícia é
      <span class="highlight">falsa</span> colando no formulário.
    </h1>
  </section>
</template>

<script>
export default {
  name: 'AppDescription',
  data() {
    return {
      animationSpeed: 1,
    };
  },
};
</script>

<style scoped lang="scss">
@import '../../styles/index';

@media only screen and (min-width: $medium) {
  .description {
    width: 70%;
    &__message {
      margin: 20px 0px;
    }
  }
}
</style>
