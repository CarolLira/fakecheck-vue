<template>
  <textarea name="news" id="" cols="30" rows="10" :placeholder="text"></textarea>
</template>

<script>
export default {
  name: 'AppTextarea',
  props: {
    text: {
      type: String,
      required: true,
    }
  }
};
</script>

<style scoped lang="scss">
@import '../../styles/index';

textarea {
  width: 100%;
  resize: none;
  height: 350px;
  padding: 1.25rem;
  border: 2px solid #202020;
  border-radius: 4px;
}

/* @media only screen (max-width: $small) {

} */

</style>
