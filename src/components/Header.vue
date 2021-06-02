<template>
  <div class="nav">
    <div class="nav-item logo">
      <NuxtLink to="/">
        <img src="/icon.png" />
      </NuxtLink>
    </div>
    <div class="nav-item">
      <NuxtLink to="/contributors">Contributors</NuxtLink>
    </div>
    <div class="nav-item">
      <a href="https://scratch.mit.edu/studios/26371714" target="_blank"
        >Scratch Studio</a
      >
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
p {
  color: black;
  text-decoration: none;
}

.nav .nav-item:not(.logo) {
  background-color: var(--brand);
  color: white;
  height: 64px;
  display: block;
  text-align: center;
  text-decoration: none;
  text-size: 55px;
  float: right;
  padding: 20px 5px 5px 10px;
}

.nav-item NuxtLink,
.nav-item a {
  color: white;
  text-decoration: none;
  text-weight: bold;
}

.nav {
  background-color: var(--brand);
  margin: 0;
  list-style-type: none;
  padding: 0;
  overflow: hidden;
  height: 64px;
  width: 100%;
}

.nav-item:not(.logo) :hover {
  background-color: rgba(0, 0, 0, 0.5);
}

.nav-item:not(.logo) NuxtLink,
.nav-item:not(.logo) a :hover {
  background-color: rgba(0, 0, 0, 0.5);
}

.nav-item a,
.nav-item NuxtLink {
  padding: 43px 16px;
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
  width: 64px;
  height: 64px;
  background-color: #4588e5;
}

.nav .nav-item.logo {
  width: 64px;
  height: 64px;
  margin-left: -16px;
}

.nav .nav-item {
  transition-duration: 0.1s;
}

.nav .nav-item * {
  transition-duration: 0.1s;
}
</style>
