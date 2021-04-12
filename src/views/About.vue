<template>
  <div class="about">
    <h1>This is an about page</h1>
    <label>Enter Name:</label>
    <input type="text" v-model="name">
    <p>{{ updatedName }}</p>
    </div>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {
      name: '',
      updatedName: '',
    };
  },
  watch: {
    name(cName, pName) {
      console.log(cName, pName);
      this.updatedName = `Mr. ${cName.toUpperCase()}`;
    },
  },
};
</script>

<style scoped>
label {
  display: block;
}
</style>
