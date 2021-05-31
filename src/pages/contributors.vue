<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black;">Contributors</h1>
      <h3>Managers</h3>
      <div>
        <template v-for="manager in managers" :key="manager.name">
          <User :user="manager.name" :bio="manager.bio" />
          <hr />
        </template>
      </div>
      <br />
      <br />
      <br />
      <h3>Curators</h3>
      <div>
        <template v-for="curator in curators" :key="curator.name">
          <User :user="curator.name" :bio="curator.bio" />
          <hr />
        </template>
      </div>
  </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Meet the contributors"
    };
  },
  async fetch() {
    let manRes = await fetch(`https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/managers.json`);

    let manJson = await manRes.json();

    this.managers = manJson;

    let curRes = await fetch(`https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/curators.json`);

    let curJson = await curRes.json();

    this.curators = curJson;
  }
};
</script>
