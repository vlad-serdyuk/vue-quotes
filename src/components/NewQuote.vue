<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset col-xs-12 col-md-6 colmd-offset-3">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset col-xs-12 col-md-6 colmd-offset-3">
                <button class="btn btn-primary" @click.prevent="addQuote">Add Quote</button>
            </div>
        </form>s
    </div>
</template>
<script>
import Quote from './Quote.vue';

export default {
    data: function() {
        return {
            quote: '',
        }
    },
    methods: {
        addQuote() {
            this.$emit('addQuote', this.quote);
            this.quote = '';
        },
    },
}
</script>