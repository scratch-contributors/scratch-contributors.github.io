<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black;">Contributors</h1>
      <h3>Managers</h3>
      <div>
        <div v-for="manager of managers" :key="manager.name">
          <User :user="manager.name" :bio="manager.bio" />
          <hr />
        </div>
      </div>
      <br />
      <br />
      <br />
      <h3>Curators</h3>
      <div>
        <div v-for="curator of curators" :key="curator.name">
          <User :user="curator.name" :bio="curator.bio" />
          <hr />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Meet the contributors",
      managers: [],
      curators: []
    };
  },
  async fetch() {
    this.managers = await fetch('https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/managers.json').then(r => r.json());

    this.curators = await fetch('https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/curators.json').then(r => r.json())
  }
};
</script>
