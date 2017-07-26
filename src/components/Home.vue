<template>
  <div class="home">
  
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            {{ heading }}
          </h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle">
              {{ subheading }}
            </h2>
          </div>
          <router-link to="learn" class="button is-large is-primary" id="learn">Learn more</router-link>
        </div>
      </div>
    </section>
  
    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1 has-text-centered">
            <i class="fa fa-5x fa-cog is-primary"></i>
          </div>
          <div class="column is-one-third-desktop">
            <p class="title">
              <strong>We provide superior logistics so that your business can succeed in a crazy world </strong>
            </p>
          </div>
          <div class="column">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam posuere nec sem quis congue. Morbi at rutrum enim</p>
          </div>
        </div>
      </div>
      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">One title Nam posuere nec sem quis congue. </p>
              <p class="subtitle">- Samuel Diogo</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Centered title Nam posuere nec sem quis congue. </p>
              <p class="subtitle">- Samuel Diogo</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">last title Nam posuere nec sem quis congue. </p>
              <p class="subtitle">- Samuel Diogo</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      heading: "Soaring to the new heights",
      subheading: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam posuere nec sem quis congue. Morbi at rutrum enim.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'

.hero
  background: url('../assets/clouds.jpg')
  background-size: cover

  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem
h2
  margin: 1.5rem 0 2rem 0 !important

.fa-cog
  font-size: 40px
#learn
  +desktop
    margin: 2rem
.pd
  +tablet
    padding: 2em 0
</style>
