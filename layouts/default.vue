<template>
  <div>
    <b-nav class="header-main">
      <b-navbar-brand>
        <b-img fluid :src="require('@/static/logo.svg')"></b-img>
      </b-navbar-brand>
      <b-nav-item class="header-items">Home</b-nav-item>
      <b-nav-item class="header-items">Investors</b-nav-item>
      <b-nav-item class="header-items">IEntreprenuers</b-nav-item>
      <b-nav-item class="header-items">Sponsors</b-nav-item>
      <b-nav-item class="header-items">Portfolio</b-nav-item>
    </b-nav>
    <nuxt />
  </div>
</template>

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
  margin: auto;
  font-size: 24px;
}

.header-main {
  position: relative;
  padding: 1rem 0;
}

.header-main::after {
  content: '';
  bottom: 0%;
  display: none;
  margin: 0 auto;
  width: 80%;
  padding-top: 0.1rem;
  border-bottom: 0.25px solid #6cd4ff;
}
</style>
