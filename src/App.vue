<template>
  <NavbarLayout />
  <router-view />
  <footer>Site by <a href='https://ifeanyilucky.vercel.app' target="_blank">Codack</a>💚</footer>
</template>

<script lang="ts">
import NavbarLayout from "./layout/Navbar.vue"
export default {
  name: 'App',
  components: {
    NavbarLayout
  }
}
</script>

<style lang="scss">
@import url('./bootstrap.css');

$primary-color: #1db227;
$primary-bold: GT Walsheim bold;
$primary-medium: GT Walsheim medium;
$primary-regular: GT Walsheim;

@font-face {
  font-family: 'GT Walsheim';
  src: url('/public/fonts/gt-walsheim-regular.ttf') format('truetype');
  font-weight: 400;
  font-display: swap;
  font-style: normal;
}

@font-face {
  font-family: 'GT Walsheim medium';
  src: url('/public/fonts/gt-walsheim-medium.ttf') format('truetype');
  font-weight: 500;
  font-display: swap;
  font-style: normal;
}

@font-face {
  font-family: 'GT Walsheim bold';
  src: url('/public/fonts/gt-walsheim-bold.ttf') format('truetype');
  font-weight: 700;
  font-display: swap;
  font-style: normal;
}

#app {
  font-family: 'GT Walsheim';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow: hidden !important;

  color: #000;

}

p {
  font-weight: 400;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 700;
  font-family: 'GT Walsheim bold';
}

.button {

  background-color: $primary-color;
  color: #fff;
  font-size: inherit;
  border-radius: 30px;
  padding: 15px 25px;
  outline: none;
  border: none;
  font-family: GT Walsheim medium;
  transition: 0.3s all ease-in-out;
  margin-right: 10px;
  border: 1px solid $primary-color;

  &:hover {
    opacity: 0.7
  }
}

.button-outline {
  background-color: transparent;

  color: $primary-color;

}

.button-white {
  background-color: #fff;
  border: 1px solid #fff;
  color: #000;

}

footer {
  text-align: center;
  margin: 20px 0;
}
</style>
