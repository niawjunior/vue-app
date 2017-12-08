<template>
  <div id="app">
      <nav class="navbar is-black">

        <div class="navbar-brand">
          <a class="navbar-item" href="http://bulma.io">
            <span>MyCompany</span>
          </a>
            <div class="navbar-burger burger" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
              <span></span>
              <span></span>
              <span></span>
            </div>
        </div>

          <div class="navbar-end navbar-menu" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
            <div class="navbar-item">
              <router-link class="navbar-item r-item" to="/">Home</router-link>
            </div>
             <hr class="navbar-divider">
            <div class="navbar-item">
              <router-link class="navbar-item r-item" to="faq">Features</router-link>
            </div>
             <hr class="navbar-divider">
            <div class="navbar-item">
              <router-link class="navbar-item r-item" to="faq">About</router-link>
            </div>
             <hr class="navbar-divider">
            <div class="navbar-item">
              <router-link class="navbar-item r-item" to="faq">FAQ</router-link>
            </div>
             <hr class="navbar-divider">
            <div class="navbar-item">
              <div class="field is-grouped">
                <p class="control">
                  <a class="button is-primary is-outlined" href="https://github.com/niawjunior/vue-app-101">
                    <span class="icon">
                      <i class="fa fa-github"></i>
                    </span>
                    <span>github</span>
                  </a>
                </p>
              </div>
            </div>
          </div>
          
      </nav>
    <router-view/>
    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>And this right here is a  spiffy footer, where you can push stuff.</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-facebook"></i></a>
            <a class="icon" href="#"><i class="fa fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data: function() {
      return {
        isActive: false
    }
  },
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
  @import '../node_modules/bulma/bulma.sass'

  a.r-item 
    color: #C1C1C1
    padding: 0.5rem 1.75rem
    +mobile
      color: gray
      &:hover
      background-color: #F1F1F1

  footer 
    background-color: $primary !important
    color: #fff

    .icon 
      color: #fff
      margin-left: 20px

</style>
