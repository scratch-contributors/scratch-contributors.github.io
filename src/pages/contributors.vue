<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black;">Contributors</h1>
      <h3>Managers</h3>
      <ul>
        <div class="user" v-for="manager in managers">
          <User :user="manager.name" :bio="manager.bio">
          <hr />
        </div>
      </ul>
      <br />
      <br />
      <br />
      <h3>Curators</h3>
      <ul>
        <div class="user" v-for="curator in curators">
          <User :user="curator.name" :bio="curator.bio">
          <hr />
        </div>
      </ul>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        title: 'Meet the contributors',
        managers: [],
        curators: []
      }
    },
    async fetch() {
      let manRes = await fetch(`https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/managers.json`);

      let manJson = await manRes.json();

      this.managers = manJson;

      let curRes = await fetch(`https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/curators.json`);

      let curJson = await curRes.json();

      this.curators = curJson;
    }
  }
</script>