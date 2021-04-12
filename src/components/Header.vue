<template>
  <div class='hello'>
    <h3>{{ text }}</h3>
    <hr/>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    text: String,
  },
};
</script>
