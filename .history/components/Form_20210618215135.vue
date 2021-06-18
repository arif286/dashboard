<template>
  <div>
    <form class="Assessment-input" action="">
      <div class="mb-3">
        <label for="Input1" class="form-label">Equipment Tag <span class="text-danger">*</span></label>
        <input id="Input1" type="text" class="form-control">
      </div>
      <div class="mb-3">
        <label for="Input2" class="form-label">Component <span class="text-danger">*</span></label>
        <input id="Input2" type="text" class="form-control">
      </div>
      <div class="mb-3">
        <label for="Input3" class="form-label">Assessment Date</label>
        <input id="Input3" type="text" class="form-control">
      </div>
      <div class="mb-3">
        <label for="Input4" class="form-label">Simulation Case</label>
        <input id="Input4" type="text" class="form-control">
      </div>
      <div class="mb-3">
        <label for="Input5" class="form-label">Assessment Interval (Years)</label>
        <input id="Input5" type="text" class="form-control">
      </div>
      <div>
        <label for="Input5" class="form-label">Units</label>
        <b-form-checkbox v-model="checked" name="check-button" switch>
          US Customary
        </b-form-checkbox>
      </div>
      <b-button class="submit-button" type="submit" variant="danger">
        START NEW CASE
      </b-button>
    </form>
  </div>
</template>
<script>
export default {
  data () {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots',
        'Beans',
        'Tomatoes',
        'Corn'
      ],
      show: true,
      checked: false
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    }
  }
}
</script>
<style>
.submit-button {
  width: 200px;
  margin-top: 60px;
}
.Assessment-input input:focus {
  border-color: red;
  box-shadow: none;
}
.Assessment-input label{
  color: gray;
}
</style>
