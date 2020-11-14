<template>
<div id="app">
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand" href="/">FoodPrint</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <router-link to="/calculator" class="nav-link">Calculator</router-link>
        <router-link to="/contact" class="nav-link">Contact</router-link>
        <router-link to="/alternatives" class="nav-link">View alternatives</router-link>
      </div>
    </div>
  </nav>
  <router-view/>
</div>
</template>
<style lang="scss" scoped>
@import "./assets/css/reset.css";
</style>
