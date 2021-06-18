<template>
  <div>
    <form action="">
      <div class="mb-3">
        <label for="Input1" class="form-label">Email address</label>
        <input id="Input1" type="email" class="form-control>
      </div>
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
}
</style>
