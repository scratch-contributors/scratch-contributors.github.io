<template>
  <div class="user">
    <p>{{ username }}</p>
    <img :src="`https://cdn2.scratch.mit.edu/get_image/user/${userid}_50x50.png`" />
    <OcularStatus :user="this.user" />
  </div>
</template>
<script>
  export default {
    props: ["user"],
    data() {
      return {
        userid: 0,
        username: ""
      }
    },
    async fetch() {
      let scratchRes = await fetch(`https://api.scratch.mit.edu/users/${this.user}`);
      let scratchJson = await scratchRes.json();

      this.userid = scratchJson.id;
      this.username = scratchJson.username;
    }
  }
</script>
