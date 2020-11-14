<template>
<div id="app">
  <div class="nav-bar">
    <div class="navcontent">
      <a class="navbrand" href="/bostonhacks/">FoodPrint</a>
      <div class="navlinks">
          <router-link to="/calculator" class="nav-link">Calculator</router-link>
          <router-link to="/contact" class="nav-link">Contact</router-link>
          <router-link to="/alternatives" class="nav-link">View alternatives</router-link>
      </div>
    </div>
  </div>
  <router-view/>
</div>
</template>
<style lang="scss" scoped>
@import "./assets/css/reset.css";

.nav-bar {
  background: #333;
  padding: 0.6vw 0;

  .navcontent {
    width: 60vw;
    margin: 0 auto;
    padding-left: 1vw;

    .navbrand {
      font-size: 1.5em;
      margin-right: 4vw;
    }

    a {
      display: inline-block;
      color: white;
      text-decoration: none;
    }

    .navlinks {
      display: inline-block;
    }
  }
}
</style>
