<template>
  <div class="container margined">
    <Header />
    <h1 style="color: black;">Contributors</h1>
    <h2>This page lists all of the contributors in our studio.</h2>
    <h3>Managers</h3>
    <ul>
      <li v-for="manager of managers">
        <img src="`https://cdn2.scratch.mit.edu/get_image/user/${manager.id}_50x50.png`" />
      </li>
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

      for (let j in manJson) {
        let man = manJson[j]
        let scratchRes = await fetch(`https://api.scratch.mit.edu/users/${man.name}`)
        let scratchJson = await scratchRes.json()

        manJson[j].id = scratchJson.id;
      }

      this.managers = manJson;

      let curRes = await fetch(`https://raw.githubusercontent.com/FunctionalMetatable/scrs/initial-files/src/static/curators.json`);

      let curJson = await curRes.json();

      this.curators = curJson;
    }
  }
</script>