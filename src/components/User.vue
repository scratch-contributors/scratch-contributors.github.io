<template>
  <div class="container">
    <header>
      <p>Joined Scratch at {{ joined }}</p>
    </header>
    <div class="wrap">
      <div class="right">
        <div class="content">
          {{ bio }}
        </div>
      </div>

      <div class="left">
        <img :src="`https://cdn2.scratch.mit.edu/get_image/user/${userid}_90x90.png`" class="pfp" />
        <a :href="`https://scratch.mit.edu/users/${username}`" class="username">{{ username }}</a>
        <OcularStatus :user="this.user" />
      </div>

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
    border-radius: 10px 10px 0px 0px;
    padding: 10px;
    font-weight: 700;
    white-space: nowrap;
    overflow: hidden;
    color: white;
  }
  .left {
    float: left;
    width: 15%;
    order: 1;
    flex: 0 0 auto;
  }
  .right {
    float: right;
    width: 85%;
    box-shadow: inset 1px 0 #e0e0e0;
    flex: 0 0 auto;
  }

  .main-content, .main-sidebar, .main-nav {
    padding: 0.75em 1em;
    overflow-wrap: break-word;
  }

  .container {
    margin-bottom: 20px;
  }

  .pfp {
    width: 90px;
    height: 90px;
  }

  .wrap {
    display: flex;
    border-left: none;
  }

  .right {
    order: 2;
    width: 85%;
    background: var(--background);
    overflow: hidden;
    display: flex;
    flex-flow: row wrap;
  }

  .content {
    display: block;
    width: 100%;
  }


</style>