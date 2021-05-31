<template>
  <i class="ocular-status"> {{ ocular.status }}
    <span class="ocular-color" style="`background-color:${ocular.color}`"></span>
  </i>
</template>
<script>
  export default {
    props: ["user"],
    data() {
      return {
        ocular: {status: "", color: ""}
      }
    },
    async fetch() {
      let res = await fetch(`https://my-ocular.jeffalo.net/api/user/${this.user}`);
      let ocular = await res.json();

      this.ocular = ocular
    },
    fetchOnServer: false
  }
</script>
<style>
.ocular-color {
  height: 10px;
  width: 10px;
  margin-left: 3px;
  background-color: rgb(32, 116, 57);
  border-radius: 50%;
  display: inline-block;
}
</style>