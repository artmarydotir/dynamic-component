<template>
    <div class="container">
        <div class="row">
            <div class="col-sm-12">
              <p>how to load dynamic component base on each button?</p>
              <button @click="selectedComponent = 'appQuote'">Quote</button>
              <button @click="selectedComponent = 'appAuthor'">Author</button>
              <button @click="selectedComponent = 'appNew'">New</button>
              <hr>
              <p>{{ selectedComponent }} </p>
              <!-- remember :is is a keyword -->
              <component :is="selectedComponent">
                <p>
                  default component
                </p>
              </component>
                <!-- <app-quote> 
                  <h2 slot="first-slot">Hi there</h2>
                </app-quote> -->
            </div>
            <div class="col-sm-12">
              <!-- u can remove comment for slot to learn more -->
                <!-- <app-quote >
                  <div slot="second-slot">
                    <h2>Hi there</h2>
                    <h3>{{  quoteTitle }} </h3>
                    <p>im a slot</p>
                  </div>
                </app-quote> -->
                <!-- default slot no name render default -->
                <!-- <app-quote>
                  <div>
                    <span> no name slot == default </span>
                  </div>
                </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
import Quote from './components/Quote.vue';
import New from './components/New.vue';
import Author from './components/Author.vue';

export default {
  data() {
    return {
      quoteTitle: 'The Quote Title',
      selectedComponent: 'appQuote'
    }
  },  
  components: {
    appQuote: Quote,
    appNew: New,
    appAuthor: Author,
  }
}
</script>

<style>

</style>
