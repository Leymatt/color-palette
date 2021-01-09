<template>
  <div id="app">
    <Main />
  </div>
</template>

<script>
import Main from "./components/main/main";
export default {
  name: 'App',
  components: {
    Main
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&display=swap');
#app {
  font-family: 'Oswald', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #131313;
}

body {
  margin: 0
}

* {
  outline: none;
  margin: 0;
  padding: 0;
  border: none;
}
</style>
