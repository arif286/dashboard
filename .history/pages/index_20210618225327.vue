<template>
  <div class="container">
    <div class="dashboard">
      <nav>
        <div id="nav-tab" class="nav nav-tabs" role="tablist">
          <button
            id="nav-home-tab"
            class="nav-link active"
            data-bs-toggle="tab"
            data-bs-target="#nav-home"
            type="button"
            role="tab"
            aria-controls="nav-home"
            aria-selected="true"
          >
            Home
          </button>
          <button
            id="nav-profile-tab"
            class="nav-link"
            data-bs-toggle="tab"
            data-bs-target="#nav-profile"
            type="button"
            role="tab"
            aria-controls="nav-profile"
            aria-selected="false"
          >
            Profile
          </button>
          <button
            id="nav-contact-tab"
            class="nav-link"
            data-bs-toggle="tab"
            data-bs-target="#nav-contact"
            type="button"
            role="tab"
            aria-controls="nav-contact"
            aria-selected="false"
          >
            Contact
          </button>
        </div>
      </nav>
      <div id="nav-tabContent" class="tab-content">
        <div id="nav-home" class="tab-pane fade show active" role="tabpanel" aria-labelledby="nav-home-tab">
          ...
        </div>
        <div id="nav-profile" class="tab-pane fade" role="tabpanel" aria-labelledby="nav-profile-tab">
          ...
        </div>
        <div id="nav-contact" class="tab-pane fade" role="tabpanel" aria-labelledby="nav-contact-tab">
          ...
        </div>
      </div>
      <b-tabs active-nav-item-class="tab-title" content-class="mt-3">
        <b-tab title="ASSESSMENT" active>
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
.dot {
  height: 10px;
  width: 10px;
  background-color: red;
  border-radius: 50%;
  display: inline-block;
}
</style>
