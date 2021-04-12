<template>
<div>
    <Header text='Please fill form to get more Info'/>
  <div class='container'>
  <form>
      <div class="form-inner">
        <h2>Contact Us</h2>
        <div class="form-group">
          <label htmlFor="name">Name:</label>
          <input
            type="text"
            id="name"
          />
          <label htmlFor="email">Email:</label>
          <input
            type="email"
            id="email"
          />
          <label>Message:</label>
          <input
            type="text"
            id="text"
          />
          <label>Additional Details:</label>
          <textarea />
        </div>
      <input v-on:click="clicked('You have submitted contact form')"
      class="btn" type="submit" value="Submit" />
      </div>
    </form>
    </div>
    </div>
</template>

<script>
import Header from '@/components/Header.vue';
import exampleMixin from '../Mixins/Mymixin';

export default {
  mixins: [exampleMixin],
  name: 'Contactus',
  components: {
    Header,
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px ;
  padding: 30px;
  border-radius: 5px;
  box-shadow: 20px 20px 60px #cccccc,
              -20px -20px 60px #ffffff;
}

.btn {
  display: block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 15px;
  font-family: inherit;
}

.form-group label {
  display: block;
  text-align: left;
}

.form-group input  {
  width: 100%;
  height: 40px;
  margin: 5px;
  padding: 3px 7px;
  font-size: 18px;
}
textarea  {
  width: 100%;
  height: 40px;
  margin: 5px;
  padding: 3px 7px;
  overflow: none;
  font-size: 18px;
}
</style>
