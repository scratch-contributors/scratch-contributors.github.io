<template>
  <footer>
    <br />
    <br />
    <hr />
    This site was proudly made by <a href="https://github.com/scratch-contributors/scratch-contributors.github.io/graphs/contributors">these scratchers</a>.
    Credit to <a href="https://jeffalo.net">Jeffalo</a> and <a href="https://theforumhelpers.github.io">The Forum Helpers</a> site for inspiration and data.
    <a class="link" @onclick="switchTheme()" href="#">switch theme (current: {{ $colorMode.preference }})</a>
  </footer>
</template>
<script>
  export default {
    methods: {
      switchTheme() {
        let currentTheme = this.$colorMode.preference;
        let themes = ['system']
        let to = themes[themes.indexOf(currentTheme) + 1]
        this.$colorMode.preference = to || 'system'
      }
    }
  }
</script>