<template>
  <div class="container">
    <Header />
    <div class="margined">
      <h1 style="color: black;">Contributors</h1>
      <h3>Managers</h3>
      <ul>
        <div class="user" v-for="manager in managers">
          <User :user="manager.name" />
          <hr />
        </div>
      </ul>
      <h3>Curators</h3>
      <ul>
        <div class="user" v-for="curator in curators">
          <User :user="curator.name" />
          <hr />
        </div>
      </ul>
  </div>
</template>
<script>
  import managers from '~/static/managers.json'
  import curators from '~/static/curators.json'
  
  export default {
    data() {
      return {
        title: 'Meet the contributors',
        managers: [],
        curators: []
      }
    },
    async fetch() {
      let manJson = JSON.parse(managers)

      this.managers = manJson;

      let curJson = JSON.parse(curators)

      this.curators = curJson;
    }
  }
</script>