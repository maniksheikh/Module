<template>
  <div class="contaier">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="NewQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to Delete It!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuoteView.vue";
import Header from "./components/HeaderView.vue";


export default {
  data: function () {
    return {
      quotes: ["Just a Quote to See Something"],
      maxQuotes: 10,
    };
  },
  methods: {
    NewQuote(quote) {
      if(this.quotes.length >= this.maxQuotes) {
        return alert('please delete Quotes first');
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  },
};
</script>

<style>
</style>
