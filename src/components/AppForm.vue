<template>
  <section class="news-form">
      <form @submit.prevent="$emit('submitEvent')" >
        <slot />
      </form>
  </section>
</template>

<script>
export default {
  name: 'Form',
  props: {
    submitEvent
  },
  emits: ['update:submitEvent']
};
</script>

<style scoped lang="scss">
@import '../../styles/index';


</style>
