<template>
  <div>
    <div id="app">
      <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/Favorites">Favorites</router-link> |
        <router-link to="/about">About</router-link>
      </div>
      <router-view/>
    </div>
    <div class="footer">
      <a href="https://github.com/BYU-CS-260-Winter-2020/lab-3b-grocery-store-PaetonM">Creative Project 3</a>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-bottom: 75px;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.footer {
  position: fixed;
  width: 100%;
  border: solid 3px;
  background-color: #42b983;
  bottom: 0px;
  text-align: center;
  height: 75px;
  line-height: 75px;
  color: black;
}
</style>
