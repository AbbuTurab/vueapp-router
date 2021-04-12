<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="dark">
        <h3 id='nav'>VUE APP</h3>
      <b-navbar-nav id='nav' class="ml-auto">
        <b-nav-item><router-link to="/">Home</router-link></b-nav-item>
        <b-nav-item><router-link to="/dashboard">Dashboard</router-link></b-nav-item>
        <b-nav-item><router-link to="/contactus">Contact Us</router-link></b-nav-item>
        <b-nav-item><router-link to="/about">About</router-link></b-nav-item>
        <b-nav-item><router-link to="/users">Users</router-link></b-nav-item>
      </b-navbar-nav>
    </b-navbar>
    <div class="main-view">
      <b-container class="bv-example-row m-0 main-container">
        <b-row class="sidebar-row">
          <b-col class="container-side-bar" cols="2"><Sidebar /></b-col>
          <b-col cols="10"><router-view /></b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue';

export default {
  name: 'App',
  components: {
    Sidebar,
  },
};
</script>

<style lang="scss" scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {

  a {
    font-weight: bold;
    color: whitesmoke;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
h3{
  text-decoration: none;
  color: whitesmoke;
}
.container-side-bar{
  border-right: 2px solid grey;
  width: 100%;
  height: 100%;
}
.sidebar-row{
  height:100%;
}

.main-view{
  height: 91vh;
}
.main-container{
  margin-right:0;
  margin-left:0;
  height:100%;
}

</style>
