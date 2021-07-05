<template>
  <div class="container">
    <div class="dashboard">
      <b-tabs active-nav-item-class="tab-title" content-class="mt-3">
        <b-tab title="ASSESSMENT" active>
          <template #title>
            ASSESSMENT <span class="dot" />
          </template>
          <div class="row mt-5">
            <div class="col-4">
              <Form />
            </div>
            <div class="col-8">
              <Table :data="dashboardData" />
            </div>
          </div>
        </b-tab>
        <b-tab>
          <template #title>
            SERVICE INFORMATION <span class="dot" />
          </template>
          <p>I'm the second tab</p>
        </b-tab>
        <b-tab>
          <template #title>
            EQUIPMENT & COATING <span class="dot" />
          </template>
          <p>I'm the tab with the very, very long title</p>
        </b-tab>
        <b-tab>
          <template #title>
            INSULATION SYSTEM <span class="dot" />
          </template>
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
/* .container {
  max-width: 1860px;
} */
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
.dot {
  height: 10px;
  width: 10px;
  background-color: red;
  border-radius: 50%;
  display: inline-block;
}
</style>
