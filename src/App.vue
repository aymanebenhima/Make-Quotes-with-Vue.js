<template>
  <div class="container">
    <app-new-quote
      @quoteAdded="newQuote"
    />
    <app-quote-grid
      :quotes="quotes"
      @quoteDeleted="deleteQuote"
    />
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'

export default {
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  },
  data() {
    return {
      quotes: [
        'Test this quote'
      ],
      maxQuotes: 10
    }
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote)
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
}
</script>

<style scoped>
.container {
  margin-top: 20px;
}
</style>
