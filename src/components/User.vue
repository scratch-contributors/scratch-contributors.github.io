<template>
  <div class="container">
    <header>
      <p>Joined at {{ joined }}</p>
    </header>
    <div class="left">
      <img :src="`https://cdn2.scratch.mit.edu/get_image/user/${userid}_50x50.png`" />
      <a :href="`https://scratch.mit.edu/users/${username}`">{{ username }}</a>
      <OcularStatus :user="this.user" />
    </div>
    <div class="right">
      {{ bio }}
    </div>
  </div>
</template>
<script>
  export default {
    props: ["user", "bio"],
    data() {
      return {
        userid: 0,
        username: "",
        joined: ""
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
  /* some styling elements taken from ocular, thanks jeffalo */
  header {
    background-color: #4D97FF;
    border-radius: 50px 50px 0px 0px;
    padding: 10px;
    font-weight: 700;
    white-space: nowrap;
    overflow: hidden;
    color: white;
  }
  .left {
    float: left;
    width: 15%;
  }
  .right {
    float: right;
    width: 85%;
    padding: .75em 1em;
    box-shadow: inset 1px 0 #e0e0e0;
    flex: 0 0 auto;
  }
  .container {
    margin-bottom: 20px;
  }
</style>