<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/calculator">Calculator</router-link> |
      <router-link to="/contact">Contact</router-link> |
      <router-link to="/alternatives">View alternatives</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {

}

#nav {

}
</style>
