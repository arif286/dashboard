<template>
  <div>
    <div class="mb-3">
      <label for="Input1" class="form-label">Email address</label>
      <input id="exampleFormControlInput1" type="email" class="form-control" placeholder="name@example.com">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
      <textarea id="exampleFormControlTextarea1" class="form-control" rows="3" />
    </div>
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
