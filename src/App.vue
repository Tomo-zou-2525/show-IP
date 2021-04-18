<template>
  <div id="app">
    <div class="bg-image">
      <ul class="navigation">
        <li class="navigation-link">
          <router-link to="/"> Home </router-link>
        </li>
        <li class="navigation-link">
          <router-link to="/search_ip"> Search_Ip </router-link>
        </li>
      </ul>
    </div>

    <router-view class="main"></router-view>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {}
};
</script>

<style lang="scss">
#app {
  height: 100vh;
}

.navigation {
  padding-top: 5%;
  display: flex;
  list-style: none;
  justify-content: flex-end;
}

.navigation-link {
  width: 100px;
  text-align: center;
  margin-right: 2rem;

  a {
    padding: 8px;
    color: #ffffff;
    text-decoration: none;
    display: block;
    font-size: 0.9rem;
    text-transform: uppercase;

    &.router-link-exact-active {
      border-bottom: 2px solid #e67e22;
    }

    &:hover {
      transition: border-bottom 0.2s;
      border-bottom: 2px solid #e67e22;
    }
  }
}

.bg-image {
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("assets/background.jpg");
  background-position: center;
  background-size: cover;
  height: 100%;
}

.main {
  height: 85%;
}
</style>
