<template>
  <div class="container">
    <div class="row">
      <div class="col-4">
        <Form />
      </div>
      <div class="col-8">
        <Table data =""/>
      </div>
    </div>
  </div>
</template>

<script>
import dashboardData from '@/assets/dashboard'
// eslint-disable-next-line semi
export default {
  data () {
    return {
      dashboardData
    }
  }
}
</script>

<style></style>
