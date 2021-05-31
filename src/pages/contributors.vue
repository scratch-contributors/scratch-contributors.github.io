<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black;">Contributors</h1>
      <h3>Managers</h3>
      <ul>
        <li v-for="manager in managers">
          <User :user="username" />
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