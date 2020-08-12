<template>
  <div class="container">
    <app-quote-grid :quotes="quotes" />
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'

export default {
  components: {
    appQuoteGrid: QuoteGrid,
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

<style scoped>
.container {
  margin-top: 20px;
}
</style>
