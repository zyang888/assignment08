<template>
  <div>
    <b-jumbotron>
      <template v-slot:header>Assignment08</template>

      <template v-slot:lead>
        <p>Use the Mixin button below and the submit button on form page to see Mixin function</p>
      </template>

      <hr class="my-4">

      <router-link to="/Grid" class="text-warning">Grid</router-link><p>Refactored into components with props & validation</p>
      <router-link to="/Images" class="text-success">Images</router-link><p>Images are all taken from an array and implemented using a v-for.</p>
      <router-link to="/Form" class="text-danger">Form</router-link><p>Creation and use of slot for header component</p>

      <b-button @click="clicked('Mixin 1 Triggered')" variant="primary" href="#">Mixin 1</b-button>
      <b-button @click="clicked('Mixin 2 Triggered')" variant="success" href="#">Mixin 2</b-button>
    </b-jumbotron>
    <!-- <img v-bind:src="image"> -->
    <img v-show="!toggle" src="../assets/OFFbulb.jpg">
    <img v-show="toggle" src="../assets/ONbulb.jpg">
  </div>
</template>

<script>
import myButton from '@/mixins/myButton'

export default {
  name: 'home',
  data () {
    return {
      toggle: false
    }
  },
  mixins: [myButton]
}
</script>
