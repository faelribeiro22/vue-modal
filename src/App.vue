<template>
  <div id="app">
    <input type="text" v-model="texto">
    <button type="button" @click="showModal = true">Abrir Modal</button>

    <modal v-if="showModal" @close="showModal = false" :text="texto">Fecha essa porra</modal>

  </div>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  name: 'app',
  components: {
    Modal
  },
  data() {
    return {
      showModal: false,
      texto: ''
    }
  }
}
</script>

<style>

</style>
