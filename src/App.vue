<template>
  <div id="app">
    <TheHeader/>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    TheHeader
}
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

:root{
  --main-bg: #f0efef;
  --main-color: #513e5e;
  --green: #22ad96;
  --white: #fefefe;
  --light-blue: #b6b8d1;
  --blue: #01afc8;
}

#app {
  font-family: 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--main-color);
}

input[type="text"]{
  border: none;
  outline: none;
  padding: 0.7rem 1rem;
  border-radius: 0.3rem;
}
</style>
