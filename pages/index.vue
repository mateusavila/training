<template>
  <div class="container">
    <Form :form="form" />
    <Submit @submit="submit" />
  </div>
</template>

<script>
export default {
  data () {
    return  {
      form: {
        name: '',
        email: ''
      }
    }
  },
  methods: {
    submit () {
      // aplica aqui a tua lógica
      console.log(this.form)
    }
  }
}
</script>

<style>
.container {
  margin: 50px auto;
  width: 300px;
}
</style>
