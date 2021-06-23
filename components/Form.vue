<template>
  <div class="fields">
    <div class="field">
      <label for="name">Nome</label>
      <input type="text" name="name" id="name" placeholder="Digite seu nome" v-model="form.name">
    </div>
    <div class="field">
      <label for="email">Email</label>
      <input type="email" name="email" id="email" placeholder="Digite seu Email" v-model="form.email">
    </div>
  </div>
</template>
<script>
  export default {
    name: 'Form',
    props: {
      form: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style>
.field {
  margin-bottom: 20px;
  width: 100%;
}
.field label, .field input {
  width: 100%;
}

</style>
