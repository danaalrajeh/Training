<template>
  <div>
    <table class="table table-hover" style="width: 100%">
      <thead>
        <th>
          <div class="table-th">
            <span class="lable">Student Name</span>
          </div>
        </th>

        <th>
          <div class="table-th">
            <span class="lable">Student ID</span>
          </div>
        </th>

        <th>
          <div class="table-th">
            <span class="lable">Total Grade</span>
          </div>
        </th>
      </thead>

      <tbody>
        <tr v-for="user in users" :key="user.sname">
          <td>
            <span>
              <span class="table-lable">{{ user.sname }}</span>
            </span>
          </td>

          <td>
            <span>
              <span class="table-lable">{{ user.sid }}</span>
            </span>
          </td>

          <td>
            <span>
              <span class="table-lable">{{ user.tgrade }}</span>
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
export default {
  name: "tables",
  data() {
    return {
      users: [
        { sname: "Lama", sid: 1, tgrade: 99 },
        { sname: "Haifa", sid: 2, tgrade: 98 },
        { sname: "Sara", sid: 3, tgrade: 99 },
      ],
    };
  },
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
