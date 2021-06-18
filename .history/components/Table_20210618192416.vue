<template>
  <div class="table-contain">
    <p class="title">
      Case History
    </p>
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
          <td>Case {{ item.case }}</td>
          <td>{{ item.status }}</td>
          <td>
            {{ item.status ? 'copy' : '' }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
      copyBtn: 'copy'
    }
  }
}
</script>
<style scoped>

.table-border tr{
 border: 1px solid #e6e2e2;
}
.table-border td{
  padding: 20px;
}
.title{
  margin-bottom: 0px;
  color: #a09b9b;
}
.table-contain {
  height: 570px;
  overflow-y: scroll;
}
</style>
