<template>
  <div class="dashboard">
    <Header text='This is the Dashboard page'/>
    <Dashboard
    msg="Vue js used to build this page" techUsed='Vuejs is a progressive
    framework for JavaScript
    used to build web interfaces and one-page applications.
    Not just for web interfaces, Vue. js is also used both for
    desktop and mobile
    app development with Electron framework.'
    />
    <Dashboard msg="History of Vuejs" techUsed='Vue was created by Evan You after working for
    Google using AngularJS in a number of projects. He later summed up his thought process:
    "I figured, what if I could just extract the part that I really liked about Angular and
    build something really lightweight."The first source code commit to the project was dated
    July 2013, and Vue was first released the following February, in 2014.'
    />
  </div>
</template>

<script>

// @ is an alias to /src
import Dashboard from '@/components/DashboardComp.vue';
import Header from '@/components/Header.vue';

export default {
  name: 'MyDashboard',
  components: {
    Dashboard,
    Header,
  },
};
</script>

<style scoped>
.dashboard{
  margin: 0 auto;
}
</style>
