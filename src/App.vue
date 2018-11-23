<template>
  <div id="app">
    
<!--
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/HelloWorld">HelloWorld</router-link>
    </div>
-->
    <router-view/>
    
  </div>
</template>

<style lang="css">
/*
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
*/
   
    
    *, *::before, *:after { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; background-color: #efefef; }
    #app { margin: 0 auto; padding: 0; max-width: 828px; width: 100%; overflow: hidden; position: relative; }
    ul, li { margin: 0; padding: 0; ;list-style: none;}
    button { margin: 0; padding: 0; }
    a { text-decoration: none;}
</style>
