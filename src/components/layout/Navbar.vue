<template>
  <section class="hero is-large">
    <div class="background-overlay">
      <div class="hero-head">
        <nav class="navbar">
          <div class="container">
            <div class="navbar-brand">
              <a class="navbar-item">
                <img
                  src="https://bulma.io/images/bulma-type-white.png"
                  alt="Logo">
              </a>
              <span
                class="navbar-burger burger"
                data-target="navbarMenuHeroB">
                <span/>
                <span/>
                <span/>
              </span>
            </div>
            <div
              id="navbarMenuHeroB"
              class="navbar-menu">
              <div class="navbar-end">
                <a class="navbar-item is-active">
                  Home
                </a>
                <a class="navbar-item">
                  Examples
                </a>
                <a class="navbar-item">
                  Documentation
                </a>
                <span class="navbar-item">
                  <a class="button is-info is-inverted">
                    <span class="icon">
                      <i class="fab fa-github"/>
                    </span>
                    <span>Download</span>
                  </a>
                </span>
              </div>
            </div>
          </div>
        </nav>
      </div>

      <div class="hero-body"/>

      <div class="hero-foot">
        <div class="container">
          <p class="title is-size-1 company-title">深圳市奥兴达科技有限公司</p>
          <p class="title company-subtitle">AXD Technology Co., Ltd.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
}
</script>

<style lang="sass" scoped>
  .hero
    background-image: url('/static/Header.jpg')
    position: relative
    background-size: cover
  .hero:before
    content: ''
    position: absolute
    top: 0
    right: 0
    left: 0
    bottom: 0
    background: rgba(0,0,0,0.7)
    opacity: 0.7
  .company-title
    margin-bottom: 0
    color: whitesmoke
    font-family: DengXian
  .company-subtitle
    margin-bottom: 1.35rem
    color: whitesmoke
    font-family: Bahnschrift
</style>
