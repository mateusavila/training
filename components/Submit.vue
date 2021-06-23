<template>
  <footer>
    <button type="submit" @click.prevent="submit">Enviar</button>
  </footer>
</template>

<script>
  export default {
    name: 'Footer',
    methods: {
      submit () { this.$emit('submit') }
    }
  }
</script>

<style>

</style>
