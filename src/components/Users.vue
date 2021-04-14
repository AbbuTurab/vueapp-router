<template>
  <div class="container">
    <h3 class="p-3 text-center">Vue.js - Display a list of items with v-for</h3>
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
          <th>Role</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in users" :key="index">
          <td>{{ user.Name }} </td>
          <td>{{ user.email }}</td>
          <td>{{ user.role }}</td>
        </tr>
      </tbody>
    </table>
    <button class="btn" v-on:click="clicked('Table has Refreshed')">Refresh Table
    </button>
    <button v-on:click='methodExample()' type="submit">Get Emails</button>
    <p v-for="(email, index) in userEmails" :key="index">{{ email }}</p>
    <p>{{ userCount }}</p>
  </div>
</template>

<script>
import exampleMixin from '../Mixins/Mymixin';

export default {
  name: 'User',
  Notes: '',
  mixins: [exampleMixin],
  computed: {
    userCount() {
      return `Total number of Users - ${this.users.length}`;
    },
  },
  data() {
    return {
      userEmails: [],
      users: [
        { Name: 'Frank', email: 'frank.murphy@test.com', role: 'Frontent Dev' },
        { Name: 'Walter', email: 'Walter.white@test.com', role: 'Fullstack Dev' },
        { Name: 'Steve', email: 'Steve.jones@test.com', role: 'Backend Dev' },
        { Name: 'Mark Raffulo', email: 'Marky.ruff@test.com', role: 'Devops' },
        { Name: 'Jessi Pinkman', email: 'Pinkman.jess@test.com', role: 'Backend Dev' },
      ],
    };
  },
  methods: {
    methodExample() {
      this.userEmails = this.users.map((value) => value.email);
    },
  },
};
</script>

<style scoped>
.btn {
  display: block;
  background: steelblue;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 15px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>
