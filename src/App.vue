<template>
  <div id="app">
    <nav class="container">
      <div class="row d-flex justify-content-center align-items-center">
        <div class="col-lg-1 d-flex justify-content-center align-items-center">
          <router-link to="/">Games</router-link>
        </div>
        <div class="col-lg-1 d-flex justify-content-center align-items-center">
          <router-link to="/movies">Movies</router-link>
        </div>
        <div class="col-lg-3">
          <h1>Hobby Tracker</h1>
        </div>
        <div class="col-lg-1 d-flex justify-content-center align-items-center">
          <router-link to="/anime">Anime</router-link>
        </div>
        <div class="col-lg-1 d-flex justify-content-center align-items-center">
          <router-link to="/about">About</router-link>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>
<script>
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px 30px 15px 30px;

  a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }

  h1 {
    cursor: pointer;
  }
}
</style>
