<template>
  <div class="container">
    <h2>Importar dado de fora</h2>
    <button @click.prevent="importData">Importar dado do banco</button>
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
      window.alert(`Nome: ${this.form.name}, E-mail: ${this.form.email}`)
    },
    async importData () {
      function mycode () {
        return new Promise((resolve, reject) => {
          return setTimeout(() => {
            resolve({
              email: 'teste@teste.com.br',
              name: 'Teste da Silva'
            })
          }, 2000);
        })
        
      }
      mycode().then(res => this.form = res)
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
