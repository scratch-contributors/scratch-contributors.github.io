<template>
  <div class="nav">
    <div class="nav-item img">
      <NuxtLink to="/">
        <img src="/icon.png" width="50px" height="50px">
      </NuxtLink>
    </div>
    <div class="nav-item">
      <NuxtLink to="/contributors">Contributors</NuxtLink>
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
h1,
h2,
h3,
h4,
h5,
h6,
a,
p :not(.nav-item *),
NuxtLink {
  color: black;
  text-decoration: none;
}

.nav .nav-item:not(.img) {
  background-color: #4d97ff;
  color: white;
  height: 65px;
  display: block;
  color: white;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
  float: left;
}

.nav {
  background-color: #4d97ff;
  margin: 0;
  list-style-type: none;
  padding: 0;
  overflow: hidden;
  height: 65px;
}

.nav-item :hover {
  background-color: #4588e5;
}

.nav-item NuxtLink, a :hover {
  background-color: #4588e5;
}

.nav-item a, NuxtLink { 
  padding: 30px 10px 30px 10px; 
  transition-duration: 0.1s; 
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
