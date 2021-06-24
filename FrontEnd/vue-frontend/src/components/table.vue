<template>
  <div>
    <table class="table table-hover" style="width: 100%">
      <thead>
        <th>
          <div class="table-th">
            <span class="lable">ID</span>
          </div>
        </th>

        <th>
          <div class="table-th">
            <span class="lable">Name </span>
          </div>
        </th>

        <th>
          <div class="table-th">
            <span class="lable">Salary</span>
          </div>
        </th>
      </thead>

      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>
            <span>
              <span class="table-lable">{{ user.id }}</span>
            </span>
          </td>

          <td>
            <span>
              <span class="table-lable">{{ user.name }}</span>
            </span>
          </td>

          <td>
            <span>
              <span class="table-lable">{{ user.salary }}</span>
            </span>
          </td>
        </tr>
      </tbody>

      <!-- <tr>
    <th>Student Name</th>
    <th>StudentID</th>
    <th>Math</th>
    <th>chemistry</th>
    <th>Physics</th>
    <th>Computer</th>
    <th>Total</th>
  </tr>
  <tr>
    <td>Dana</td>
    <td>1</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>40</td>
  </tr>
  <tr>
    <td>Hana</td>
    <td>2</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>40</td>
  </tr>
  <tr>
    <td>Sara</td>
    <td>3</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>10</td>
    <td>40</td>
  </tr>-->
    </table>
  </div>
</template>

<script>
/*export async function getAllUsers() {

    const response = await fetch('/http://localhost:3001/employees');
    return await response.json();
}*/



/*export async function createUser(data) {
    const response = await fetch('/http://localhost:3001/employees', {
        method: 'POST',
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify({user: data})
      })
    return await response.json();
}*/

const axios = require('axios');


export default {
  name: "tables",
  data() {
    return {
      users: [
        
      ],
    };
  },
   mounted () {
    axios
      .get('http://localhost:3001/employees')
      .then(response => (this.users = response.data))
  }
};
</script>

<style >
.table,th,tr,td {
  text-align: center;
  border: 1px solid;
  color: rgb(73, 7, 42);
}
.table {
  margin-top: 10%;
}

</style>
