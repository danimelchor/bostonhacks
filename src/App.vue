<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/calculator">Calculator</router-link>
      <router-link to="/contact">Contact</router-link>
      <router-link to="/alternatives">View alternatives</router-link>
    </div>
    <router-view />
  </div>
</template>
<style lang="scss">
@import './assets/css/reset.css';

$bg : #222;

#app {
}

#nav {
  background-color: $bg;
  text-align: center;

  a {
    color: white;
    display: inline-block;
    text-decoration: none;
    padding: 1vw;
  }

  a:hover {
    color: #333;
  }
}
</style>
