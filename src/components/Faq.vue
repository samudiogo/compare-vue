<template>
  <div class="faq">
    <div class="container">
      <section class="section">
        <h1 class="title">FAQ</h1>
        <h2 class="subtitle is-4">Lorem ispum and all of that jazz.</h2>
  
        <div class="columns" v-if="faqs && faqs.length">
          <div class="column is-one-third" v-for="f of faqs">
            <div class="card">
              <div class="card-content">
                <p class="title">{{f.title}}</p>
                <p class="answer">{{ f.body}}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
<script>
import axios from 'axios';
export default {
  name: 'faq',
  data: () => ({
    faqs: [],
    errors: []
  }),
  created() {
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(r => {
        this.faqs = r.data.slice(0, 9);
      }).catch(e => { this.errors.push(e); });
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'


.pd
  padding: 2.5em 0 1.5em 0
.answer
  margin-top: 10px !important
  color: gray
.columns
  flex-wrap: wrap
</style>
