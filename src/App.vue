<template>
  <router-view />
</template>

<style lang="scss">
@import 'styles/index.scss';

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body,
input,
textarea,
button {
  font-family: $OpenSans;
  font-weight: 400;
}
h1,
h2,
h3,
h4,
h5,
h6,
strong {
  font-family: $Poppins;
  font-weight: 500;
}
button {
  cursor: pointer;
}
[disabled] {
  opacity: 0.6;
  cursor: not-allowed;
}

/* body {
  background-color: $sauvignon;
} */

html {
  @media only screen and (min-width: $x-small) {
    font-size: 87.5%;
  }
  @media only screen and (min-width: $large) {
    font-size: 100%;
  }
  @media only screen and (min-width: $extra-large) {
    font-size: 112.5%;
  }
}
</style>
