<template>
  <footer class="margined">
    <br />
    <br />
    <hr />
    <p>This site was proudly made by <a href="https://github.com/scratch-contributors/scratch-contributors.github.io/graphs/contributors">these scratchers</a>.</a></p>
    <br />
    <p>Credit to <a href="https://jeffalo.net">Jeffalo</a> and <a href="https://theforumhelpers.github.io">The Forum Helpers</a> site for inspiration and data.</p>
    <br />
    <button class="link" @click="switchTheme()" href="#">switch theme (current: {{ $colorMode.preference }})</button>
    <br />
    <br />
    <br />
  </footer>
</template>
<script>
  export default {
    methods: {
      switchTheme() {
        let currentTheme = this.$colorMode.preference;
        let themes = ['system', 'light', 'dark']
        let to = themes[themes.indexOf(currentTheme) + 1]
        this.$colorMode.preference = to || 'system'
      }
    }
  }
</script>
<style scoped>
  button.link {
    border: none;
    background-color: none;
    cursor: pointer;
    font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif
  }
</style>
