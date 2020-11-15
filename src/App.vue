<template>
<div id="app">
  <div class="nav-bar">
    <div class="navcontent">
      <router-link class="navbrand" to="/">FoodPrint</router-link>
      <div class="navlinks">
          <router-link to="/calculator" class="nav-link">Calculator</router-link>
          <router-link to="/contact" class="nav-link">Contact</router-link>
          <router-link to="/alternatives" class="nav-link">View alternatives </router-link>
          <router-link to="/calculator" class="nav-link-mobile"><i class="fas fa-calculator"></i></router-link>
          <router-link to="/contact" class="nav-link-mobile"><i class="fas fa-comment"></i></router-link>
          <router-link to="/alternatives" class="nav-link-mobile"><i class="fas fa-carrot"></i></router-link>
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
      vertical-align: middle;
      color: white;
      text-decoration: none;
    }

    .navlinks {
      display: inline-block;
    }

    .nav-link {
      display: inline-block;
      color: white;
      text-decoration: none;
    }

    .nav-link-mobile {
      display: none;
      color: white;
      text-decoration: none;
    }
  }
}

@media (max-width: 600px) {
  .nav-bar {
    position: fixed;
    top: 0;
    z-index: 100;

    .navcontent {
      width: 100vw;
      padding: 3vw 7vw;

      .navlinks {
        vertical-align: middle;
        float: right;
      }

      .navbrand {
        font-size: 1.8em;
        margin-right: 8vw;
      }

      .nav-link {
        display: none;
      }

      .nav-link-mobile {
        display: inline-block;
        padding: 0 3vw;
        font-size: 1.5em;
      }
    }
  }
}
</style>

<script>
export default {
  name: "App"
};
</script>
