<template>
  <header class="header">
    <img :src="images.robotIcon" alt="Logo" />
    <h2>FakeCheck</h2>
  </header>
</template>

<script>
import robotIcon from '../assets/robotIcon.png';

export default {
  name: 'AppHeader',
  data() {
    return {
      images: {
        robotIcon,
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import '../../styles/index';

.header {
  display: flex;
  padding: 1.2rem 2rem;
  align-items: center;
  background-color: $cerulean-light;
  img {
    width: 2.5rem;
  }
  h2 {
    color: $light-coral;
    padding: 0 1rem;
    font-size: 1.5rem;
  }
}
</style>
