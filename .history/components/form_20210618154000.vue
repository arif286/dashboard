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
      <b-form-group id="input-group-2" label="Assessment Date" label-for="input-2">
        <b-form-input
          id="input-2"
          required
        />
      </b-form-group>
      <b-form-group id="input-group-2" label="Simulation Case" label-for="input-2">
        <b-form-input
          id="input-2"
          required
        />
      </b-form-group>
      <b-form-group id="input-group-2" label="Assessment interval (Years)" label-for="input-2">
        <b-form-input
          id="input-"
          required
        />
      </b-form-group>

      <b-button type="submit" variant="danger">
        Submit
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
<style></style>
