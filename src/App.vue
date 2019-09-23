<template>
    <div class="container">
        <app-header
            :quoteCount="quotes.length"
            :maxQuotes="maxQuotes"
        />
        <app-new-quote @addQuote="addQuote"></app-new-quote>
        <app-quote-grid 
            :quotes="quotes"
            @deleteQuote="deleteQuote"
        ></app-quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Note:</div>
            </div>
        </div>
    </div>
</template>

<script>

import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';
    
export default {
    data: function() {
        return {
            quotes: ['test quote'],
            maxQuotes: 10,
        }
    },
    components: {
        appQuoteGrid: QuoteGrid,
        appNewQuote: NewQuote,
        appHeader: Header,
    },
    methods: {
        addQuote(newQuote) {
            if (this.quotes.length >= this.maxQuotes) {
                return alert('Please delete quotes first!');
            }
            this.quotes.push(newQuote);
        },
        deleteQuote(index) {
            this.quotes.splice(index, 1);
        },
    },
}
</script>

<style>
</style>
