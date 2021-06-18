<template>
  <div class="container">
    <div class="row mt-4">
      <div class="col-4">
        <Form />
      </div>
      <div class="col-8">
        <Table :data="dashboardData" />
      </div>
    </div>
  </div>
</template>

<script>
import { dashboardData } from '@/assets/dashboard.js'
// eslint-disable-next-line semi
export default {
  data () {
    return { dashboardData }
  }
}
</script>

<style>
.container {
  max-width: 1860px;
}
</style>
