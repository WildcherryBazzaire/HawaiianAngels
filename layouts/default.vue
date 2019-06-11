<template>
  <div>
    <b-navbar ref="headerMain" class="header-main px-4 pb-4 py-2">
      <b-navbar-brand>
        <b-img fluid :src="require('@/static/logo.svg')"></b-img>
      </b-navbar-brand>
      <b-navbar-nav ref="headerContent" class="float-right">
        <b-nav-item class="header-items px-5" to="/">Home</b-nav-item>
        <b-nav-item class="header-items px-5" to="/investor"
          >Investors</b-nav-item
        >
        <b-nav-item class="header-items px-5" to="/entrepreneurs"
          >Entreprenuers</b-nav-item
        >
        <b-nav-item class="header-items px-5" to="/sponsors"
          >Sponsors</b-nav-item
        >
        <b-nav-item class="header-items px-5" to="/portfolio"
          >Portfolio</b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>
    <nuxt />
  </div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'
export default {
  beforeMount() {
    AOS.init()
    // window.addEventListener('scroll', e => {
    //   const scrollPos = window.scrollY
    //   const winHeight = window.innerHeight
    //   const docHeight = document.documentElement.scrollHeight
    //   const perc = (100 * scrollPos) / (docHeight - winHeight)
    //   if (perc >= 26) {
    //     this.$refs.headerMain.className =
    //       'header-main-scroll navbar px-4 py-1 navbar-light navbar-expand'
    //     this.$refs.headerContent.className = 'navbar-nav float-right my-auto'
    //   }
    // })
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: #fcfcfc;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.header-items {
  position: relative;
  font-size: 18px;
}

.header-items > a {
  color: #4f4e4c;
}

.header-main {
  position: relative;
}

.header-main::after {
  content: '';
  bottom: 5%;
  position: absolute;
  width: 75%;
  padding-top: 0.1rem;
  left: 50%;
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
  background: -webkit-gradient(
    radial,
    50% 50%,
    0,
    50% 50%,
    350,
    from(#db4c40),
    to(#fcfcfc)
  );
}

.header-main-scroll {
  background: #b70304;
  position: fixed;
  z-index: 3;
  width: 100%;
}

.header-main-scroll > ul > li > a {
  color: #fcfcfc;
}

.header-main-scroll::after {
  display: none;
}

#oof {
  position: fixed;
  top: 0%;
  color: blue;
}
</style>
