<template>
  <header>
    <p>Joined at {{ joined }}</p>
  </header>
  <div class="left">
    <img :src="`https://cdn2.scratch.mit.edu/get_image/user/${userid}_50x50.png`" />
    <p>{{ username }}</p>
    <OcularStatus :user="this.user" />
  </div>
  <div class="right">
    <Bio :bio="bio" />
  </div>
</template>
<script>
  export default {
    props: ["user", "bio"],
    data() {
      return {
        userid: 0,
        username: ""
      }
    },
    async fetch() {
      console.log(`Fetching => ${this.user}`)
      let scratchRes = await fetch(`https://api.scratch.mit.edu/users/${this.user}`);
      let scratchJson = await scratchRes.json();

      this.userid = scratchJson.id;
      this.username = scratchJson.username;
      this.joined = (new Date(scratchJson.history.joined)).toString()
    }
  }
</script>
<style scoped>
  header {
    background-color: #4D97FF;
    border-radius: 50px 50px 0px 0px;
    padding-left: 10%;
  }
  .left {
    float: left;
    width: 30%;
  }
  .right {
    float: right;
    width: 69%;
  }
</style>