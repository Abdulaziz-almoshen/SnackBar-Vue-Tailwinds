<template>
  <snack />
  <a href="#" @click.prevent="doSomething">Trigger snack</a>
</template>

<script>
import { mapActions } from 'vuex'
import Snack from "@/components/Snack";
export default {
  name: 'App',

  components: {
    Snack
  },

  methods: {
    ...mapActions({
      snack: 'snack/snack'
    }),

    doSomething () {
      this.snack({
        text: 'This is a snack!',
        delay: 1000
      })
    }
  }
}
</script>

<style src="./assets/css/App.css" />