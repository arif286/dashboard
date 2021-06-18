<template>
  <div>
    <b-form v-if="show" @submit="onSubmit">
      <b-form-group
        id="input-group-1"
        label="Equipment Tag"
        label-for="input-1"
      >
        <b-form-input id="input-1" v-model="form.email" type="email" required />
      </b-form-group>

      <b-form-group id="input-group-2" label="Component" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
        />
      </b-form-group>
      <b-form-group id="input-group-3" label="Assessment Date" label-for="input-3">
        <b-form-input
          id="input-3"
          required
        />
      </b-form-group>
      <b-form-group id="input-group-4" label="Simulation Case" label-for="input-4">
        <b-form-input
          id="input-4"
          required
        />
      </b-form-group>
      <b-form-group id="input-group-2" label="Assessment interval (Years)" label-for="input-5">
        <b-form-input
          id="input-5"
          required
        />
      </b-form-group>

      <b-button class="submit-button" type="submit" variant="danger">
        S
      </b-button>
    </b-form>
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
      show: true
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
.submit-button{
  width: 200px;
}
</style>
