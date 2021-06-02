<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
.light-mode {
  --sidebar-border: #e0e0e0;
  --background: #fffdd0;
  --sidebar-background: #f2f2f2;
  --sidebar-border: #e0e0e0;
  --brand: #4d97ff;
  --text: #575e75;
}

.dark-mode {
  --sidebar-border: #9b9a9a;
  --background: #111111;
  --sidebar-background: #787474;
  --sidebar-border: #817a7a;
  --brand: #657995;
  --text: white;
}

html,
body {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  color: var(--text);
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  margin: 0;
  text-decoration: none;
  background-color: var(--background);
  transition-duration: 0.1s;
}

.margined {
  margin-left: 22.5px;
}

* {
  box-sizing: border-box;
}

NuxtLink,
a {
  text-decoration: none;
  font-weight: bold;
  color: #3b7ee8;
}
</style>
