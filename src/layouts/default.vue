<template>
  <Nuxt />
</template>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  color: black;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

h1, h2, h3, h4, h5, h6, a, p :not(.nav-item *) {
  color: black;
}

.nav .nav-item:not(.img) {
  background-color: #4D97FF;
  color: white;
  height: 65px;
  display: block;
  color: white;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
  padding: 22px 16px;
  float: left;
}

.nav {
  background-color: #4D97FF;
  margin: 0;
  list-style-type: none;
  padding: 0;
  overflow: hidden;
  height: 65px;
}

.nav-item :hover {
  background-color: #4588E5;
}

.nav-item NuxtLink :hover {
  background-color: #4588E5;
}

.nav .nav-item.img {
  display: block;
  color: white;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
  padding: 0px 0px;
  float: left;
  background-color: #151618;
}
</style>
