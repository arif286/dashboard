<template>
  <div class="table-contain">
    <p class="title">
      Case History
    </p>
    <table class="w-100 table-border">
      <tbody>
        <tr v-for="item in data" :key="item.id">
          <td>{{ item.equipmentTag }}</td>
          <td>{{ item.component }}</td>
          <td>{{ item.assessmentDate }}</td>
          <td>Case {{ item.case }}</td>
          <td>
            <span>
              {{ item.status }}
            </span>
          </td>
          <td>
            <span :class="item.copy ? 'copy-btn' : ''">{{ item.copy ? 'copy' : '' }}</span>
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
  height: 606px;
  overflow-y: scroll;
}
.copy-btn{
  background-color: #007bff;
  padding: 1px 20px;
  color: white;
  border-radius: 5px;
}
.status-draft{
  color: #007bff;
}
.status-process{
  color: orange;
}
.status-success{
  color: greenyellow;
}
.status-failure{
  color: red;
}
</style>
