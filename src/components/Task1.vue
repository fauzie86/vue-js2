
<template>
  <div>
    <h1>Form</h1>
    <div class="form-container">
      <label>Email:</label>
      <input type="text" placeholder="Enter your email" v-model="email" />
      <br>

      <label>Password:</label>
      <input type="text" placeholder="Enter password" v-model="password" />
      <br>

      <label>Message:</label>
      <input type="text" placeholder="Enter your message" v-model="message" />
      <br>

      <button @click="getdata">Get values</button>
    </div>

    <div v-if="displayData">
      <h2>Printed Data</h2>
      <table>
        <thead>
          <tr>
            <th>Email</th>
            <th>Password</th>
            <th>Message</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ email }}</td>
            <td>{{ password }}</td>
            <td>{{ message }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "TwoWay",
  data() {
    return {
      email: null,
      password: null,
      message: null,
      displayData: false,
    };
  },
  methods: {
    getdata() {
      console.log("Values: ", this.email, this.password, this.message);
      this.displayData = true;
    },
  },
};
</script>

<style>
.form-container {
  max-width: 400px;
  margin: auto;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
}

button {
  background-color: #4caf50;
  color: white;
  padding: 10px;
  border: none;
  cursor: pointer;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

table, th, td {
  border: 1px solid #ddd;
}

th, td {
  padding: 10px;
  text-align: left;
}

th {
  background-color: #4caf50;
  color: white;
}
</style>





