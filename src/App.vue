<template>
  <div id="app" class="container">
    <app-quote />
  </div>
</template>

<script>
import Quote from './components/Quote.vue'

export default {
  name: 'App',
  components: {
    appQuote: Quote,
  },
  data() {
    return {
      quotes: [
        'Test this quote'
      ],
      maxQuotes: 10
    }
  },
}
</script>

<style>

</style>
