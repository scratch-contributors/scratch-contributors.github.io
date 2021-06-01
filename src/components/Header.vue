<template>
  <div class="nav">
    <div class="nav-item logo">
      <NuxtLink to="/">
        <img src="/scrs/icon.png" />
      </NuxtLink>
    </div>
    <div class="nav-item">
      <NuxtLink to="/contributors"><span>Contributors</span></NuxtLink>
    </div>
    <div class="nav-item">
      <a href="https://scratch.mit.edu/studios/26371714">Scratch Studio</a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h1, h2, h3, h4, h5, h6, p {
  color: black;
  text-decoration: none;
}

.nav .nav-item:not(.logo) {
  background-color: #4d97ff;
  color: white;
  height: 64px;
  display: block;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
}

.nav .nav-item span {
  color: white;
  text-decoration: none;
  text-weight: bold;
}

.nav {
  background-color: #4d97ff;
  margin: 0;
  list-style-type: none;
  padding: 0;
  overflow: hidden;
  height: 64px;
  width: 100%;
}

.nav-item :hover {
  background-color: #4588e5;
}

.nav-item NuxtLink, .nav-item a :hover {
  background-color: #4588e5;
}

.nav-item a, .nav-item NuxtLink { 
  padding: 30px 10px 30px 10px;
  transition-duration: 0.1s; 
}

.nav .nav-item.logo {
  display: block;
  color: white;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
  padding: 0px 0px;
  float: left;
  background-color: #151618;
}

.nav .nav-item.logo img {
  width: 100px;
  height: 99.999px;
  background-color: #4588e5;
}

.nav .nav-item {
  transition-duration: 0.1s; 
}
</style>
