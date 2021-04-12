<template>
  <div class='sidebar'>
    <h3>Sidemenu</h3>
    <div class="link-items">
    <a href="#">Latest Posts</a>
    <a href="#">News</a>
    <a href="#">Careers</a>
    <a href="#">Services</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.link-items{
a {
  display: block;
  padding: 10px;
  color: black;
  text-decoration: none;
}
}
</style>
