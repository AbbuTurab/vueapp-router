<template>
  <div class='hello'>
    <h1>{{ welcome }}</h1>
    <hr/>
    <h2>{{ msg }}</h2>
    <em>{{ techUsed }}</em>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  props: {
    welcome: String,
    msg: String,
    techUsed: String,
    message: new Date().toLocaleString(),
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
.description{
  text-align: center;
}

</style>
