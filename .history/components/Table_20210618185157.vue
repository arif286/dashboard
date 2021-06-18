<template>
  <table class="w-100 table-border">
    <!-- <thead>
        <tr>
          <th className="text-secondary" scope="col">
            Name
          </th>
          <th className="text-secondary" scope="col">
            Email Id
          </th>
          <th className="text-secondary" scope="col">
            Service
          </th>
          <th className="text-secondary" scope="col">
            pay with
          </th>
          <th className="text-secondary" scope="col">
            status
          </th>
        </tr>
      </thead> -->
    <tbody>
      <tr v-for="item in data" :key="item.id">
        <td>{{ item.equipmentTag }}</td>
        <td>{{ item.component }}</td>
        <td>{{ item.assessmentDate }}</td>
        <td>{{ item.case }}</td>
        <td>{{ item.status }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      required: true
    }
  }
}
</script>
<style scoped>

.table-border tr{
 border: 1px solid gray;
}
.table-border td
</style>
