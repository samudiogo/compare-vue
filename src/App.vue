<template>
  <div id="app">
    <div class="nav has-shadow">
      <div class="container">
        <div class="nav-left">
          <router-link to="/" class="nav-item"> My Company</router-link>
        </div>
  
        <span class="nav-toggle" v-on:click="toggleNav" v-bind:class="{'is-active': isActive}">
          <span></span>
          <span></span>
          <span></span>
        </span>
        <div class="nav-right nav-menu" v-bind:class="{'is-active': isActive}">
          <router-link to="/" class="nav-item r-item">Home</router-link>
          <router-link to="/faq" class="nav-item r-item">Features</router-link>
          <router-link to="/faq" class="nav-item r-item">About</router-link>
          <router-link to="/faq" class="nav-item r-item">Faq</router-link>
          <div class="nav-item">
            <p class="control">
              <router-link to="faq" class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Join Now</span>
              </router-link>
            </p>
          </div>
        </div>
      </div>
    </div>
  
    <router-view></router-view>
  
    <footer class="footer is-primary">
  
      <div class="container">
        <div class="columns">
          <div class="column">Lorem ipsum dolor sit amet, consectetur adipiscing elit</div>
          <div class="column has-text-right">
            <a href="#" class="icon">
              <i class="fa fa-facebook"></i>
            </a>
            <a href="#" class="icon">
              <i class="fa fa-twitter"></i>
            </a>
          </div>
        </div>
      </div>
  
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function () {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

$cOne: #C1C1C1

.nav
  background-color: #383838
  a:hover
      color: gray !important

  .nav-left a
      color: #FFF !important
      font-weight: bold

  a.r-item
    color: #C1C1C1 !important
    padding: 0.5rem 1.75rem
    +mobile
      color: gray !important
      &:hover
        background-color: #F1F1F1 !important

  .nav-toggle span
      background-color: $cOne

footer
  background-color: $primary !important
  color: #FFF

  .icon
    color: #FFF
    margin-left: 20px
</style>
