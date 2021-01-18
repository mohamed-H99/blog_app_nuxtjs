<template>
  <header id="tm-header" class="tm-header">
    <div class="tm-header-wrapper">
      <button
        class="navbar-toggler"
        type="button"
        aria-label="Toggle navigation"
        @click.stop="navbarToggle"
      >
        <i class="fas fa-bars"></i>
      </button>
      <div class="tm-site-header">
        <div class="mb-3 mx-auto tm-site-logo">
          <i class="fas fa-rss fa-2x"></i>
        </div>
        <h1 class="text-center">EXtra Blog</h1>
      </div>
      <nav id="tm-nav" class="tm-nav">
        <ul>
          <nuxt-link
            tag="li"
            to="/"
            exact-active-class="active"
            class="tm-nav-item"
          >
            <a href="#" class="tm-nav-link" @click="removeShow">
              <i class="fas fa-home"></i>
              Blog Home
            </a>
          </nuxt-link>
          <nuxt-link
            tag="li"
            to="/post"
            exact-active-class="active"
            class="tm-nav-item"
          >
            <a href="#" class="tm-nav-link" @click="removeShow">
              <i class="fas fa-pen"></i>
              Single Post
            </a>
          </nuxt-link>
          <nuxt-link
            tag="li"
            to="/about"
            exact-active-class="active"
            class="tm-nav-item"
          >
            <a href="#" class="tm-nav-link" @click="removeShow">
              <i class="fas fa-users"></i>
              About EXtra
            </a>
          </nuxt-link>
          <nuxt-link
            tag="li"
            to="/contact"
            exact-active-class="active"
            class="tm-nav-item"
          >
            <a href="#" class="tm-nav-link" @click="removeShow">
              <i class="far fa-comments"></i>
              Contact Us
            </a>
          </nuxt-link>
        </ul>
      </nav>
      <div class="tm-mb-65">
        <a rel="nofollow" href="https://facebook.com" class="tm-social-link">
          <i class="fab fa-facebook tm-social-icon"></i>
        </a>
        <a href="https://twitter.com" class="tm-social-link">
          <i class="fab fa-twitter tm-social-icon"></i>
        </a>
        <a href="https://instagram.com" class="tm-social-link">
          <i class="fab fa-instagram tm-social-icon"></i>
        </a>
        <a href="https://linkedin.com" class="tm-social-link">
          <i class="fab fa-linkedin tm-social-icon"></i>
        </a>
      </div>
      <p class="tm-mb-80 pr-5 text-white">
        EXtra Blog is a multi-purpose HTML template website. Left side is a
        sticky menu bar. Right side content will scroll up and down.
      </p>
    </div>
  </header>
</template>

<script>
// $(function () {
//   $('.navbar-toggler').on('click', function (e) {
//     $('.tm-header').toggleClass('show')
//     e.stopPropagation()
//   })

//   $('html').click(function (e) {
//     var header = document.getElementById('tm-header')

//     if (!header.contains(e.target)) {
//       $('.tm-header').removeClass('show')
//     }
//   })

//   $('#tm-nav .nav-link').click(function (e) {
//     $('.tm-header').removeClass('show')
//   })
// })
export default {
  name: 'Sidebar',
  methods: {
    navbarToggle() {
      document.querySelector('.tm-header').classList.toggle('show')
    },
    removeShow() {
      document.querySelector('.tm-header').classList.remove('show')
    }
  },
}
</script>
