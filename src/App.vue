<template>
  <div id="app" class="blue-grey darken-4">
    <img class="logo" src="@/assets/header-log.jpg" alt="" />
    <h3 class="white-text">
      Dreamer's <br />
      diary
    </h3>
    <div id="nav" class="white-text">
      <router-link class="white-text" to="/">Home</router-link>
      |
      <router-link class="white-text" to="/addPost">addPost</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Neucha&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Caveat:wght@400;600&display=swap");
*{
  box-sizing: initial;
}
#app {
  font-family: "Caveat";
}
.logo {
  width: 90px;
  height: 90px;
}
h3 {
  display: inline-block;
  vertical-align: bottom;
  font-size: 20px;
}
#nav {
  float: right;
  margin-right: 50px;
  margin-top: 50px;
  font-family: "Neucha";
}
a {
  text-decoration: none;
}
</style>
