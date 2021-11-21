<template>
  <div class="home">
    <AppHeader />
    <main>
      <div class="home__form-container">
        <AppDescription />
        <AppForm>
          <AppTextarea text="Cole sua notícia aqui" />
          <AppButton text="Checar" />
        </AppForm>
      </div>
    </main>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
import AppDescription from '@/components/AppDescription.vue';
import AppForm from '@/components/AppForm.vue';
import AppTextarea from '@/components/AppTextarea.vue';
import AppButton from '@/components/AppButton.vue';

export default {
  name: 'Home',
  components: {
    AppHeader,
    AppDescription,
    AppForm,
    AppTextarea,
    AppButton,
  },
};
</script>

<style lang="scss" scoped>
@import '../../styles/index';

main {
  padding: 2.5rem;
}

@media only screen and (min-width: $medium) {
  .home {
    &__form-container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
}
</style>
