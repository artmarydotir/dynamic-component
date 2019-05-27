<template>
    <div class="container">
        <div class="row">
            <div class="col-sm-12">
                <app-quote> 
                  <h2 slot="first-slot">Hi there</h2>
                </app-quote>
            </div>
            <div class="col-sm-12">
                <app-quote >
                  <div slot="second-slot">
                    <h2>Hi there</h2>
                    <h3>{{  quoteTitle }} </h3>
                    <p>im a slot</p>
                  </div>
                </app-quote>
            </div>
        </div>
    </div>
</template>

<script>
import Quote from './components/Quote.vue';

export default {
  data() {
    return {
      quoteTitle: 'The Quote Title',
    }
  },  
  components: {
    appQuote: Quote,
  }
}
</script>

<style>

</style>
