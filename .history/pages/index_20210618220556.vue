<template>
  <div class="container">
    <div class="dashboard">
      <b-tabs active-nav-item-class="tab-title" content-class="mt-3">
        <b-tab title="ASSESSMENT" active>
          <b-badge>New</b-badge>
          <div class="row mt-5">
            <div class="col-4">
              <Form />
            </div>
            <div class="col-8">
              <Table :data="dashboardData" />
            </div>
          </div>
        </b-tab>
        <b-tab title="SERVICE INFORMATION">
          <p>I'm the second tab</p>
        </b-tab>
        <b-tab title="EQUIPMENT & COATING">
          <p>I'm the tab with the very, very long title</p>
        </b-tab>
        <b-tab title="INSULATION SYSTEM">
          <p>I'm a disabled tab!</p>
        </b-tab>
        <b-tab title="INSPECTION">
          <p>I'm a Inspection!</p>
        </b-tab>
      </b-tabs>
      <div class="radial-progress">
        <radial-progress-bar
          :diameter="70"
          :completed-steps="completedSteps"
          :total-steps="totalSteps"
          inner-stroke-color="grey"
          start-color="red"
          stop-color="red"
        >
          <span>50%</span>
        </radial-progress-bar>
      </div>
    </div>
  </div>
</template>

<script>
import { dashboardData } from '@/assets/dashboard.js'
import RadialProgressBar from 'vue-radial-progress'
// eslint-disable-next-line semi
export default {
  components: {
    RadialProgressBar
  },
  data () {
    return {
      dashboardData,
      completedSteps: 3,
      totalSteps: 6
    }
  }
}
</script>

<style>
.container {
  max-width: 1860px;
}
.tab-title{
  color: red !important;
  font-weight: 500;
  border: none !important;
  border-bottom: 1px solid red !important;

}
a{
  color: gray;
}
a:hover{
  color: gray;
  border-color: none;
}
.dashboard{
  position: relative;
}
.radial-progress{
  position: absolute;
  top: 39px;
  right: 12px;
}
</style>
