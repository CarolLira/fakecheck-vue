<template>
  <section class="news-form">
      <form>
        <slot />
      </form>
  </section>
</template>

<script>
export default {
  name: 'Form',
};
</script>

<style scoped lang="scss">
@import '../../styles/index';

.news-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  form {
    width: 100%;
    display: grid;
    grid-template-rows: auto;
    row-gap: 15px;
  }
}

@media only screen and (min-width: $medium) {
  .news-form {
    width: 70%;
  }
}
</style>
