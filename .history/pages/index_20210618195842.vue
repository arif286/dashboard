<template>
  <div class="container">
    <div>
      <b-tabs content-class="mt-3" fill>
        <b-tab title="First" active>
          <p>I'm the first tab</p>
        </b-tab>
        <b-tab title="Second">
          <p>I'm the second tab</p>
        </b-tab>
        <b-tab title="Very, very long title">
          <p>I'm the tab with the very, very long title</p>
        </b-tab>
        <b-tab title="Disabled" disabled>
          <p>I'm a disabled tab!</p>
        </b-tab>
      </b-tabs>
    </div>
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
