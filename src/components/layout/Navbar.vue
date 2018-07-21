<template>
  <section class="hero is-large video">
    <div class="background-overlay">
      <div class="hero-video">
        <video
          id="bgvid"
          playsinline
          autoplay
          muted
          loop>
          <source
            src="https://s3.ap-northeast-2.amazonaws.com/axd-tech-web-portal/SMT+Machine_1.mp4"
            type="video/mp4">
        </video>
      </div>
      <div class="hero-head">
        <nav class="navbar">
          <div class="container thick-bar">
            <div class="navbar-brand">
              <a class="navbar-item">
                <img
                  src="/static/Logo.svg">
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
                <router-link
                  to="/"
                  class="navbar-item customed-item">
                  主页
                </router-link>
                <router-link
                  to="/contact"
                  class="navbar-item customed-item">
                  联系我们
                </router-link>
                <div class="navbar-item is-hoverable">
                  <a class="navbar-link">
                    <p class="language">更改语言</p>
                  </a>
                  <div class="navbar-dropdown is-boxed">
                    <a class="navbar-item">
                      <img
                        class="flag"
                        src="/static/CN.png">
                      简体中文
                    </a>
                    <a class="navbar-item">
                      <img
                        class="flag"
                        src="/static/HK.png">
                      繁体中文
                    </a>
                    <a class="navbar-item">
                      <img
                        class="flag"
                        src="/static/EN.png">
                      English
                    </a>
                  </div>
                </div>
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
    background-image: url('https://rpmy9a.bn.files.1drv.com/y4mVP3Rg-VZAbKSbIKINcmfeEE3rAXKcq6zu1eMMjVZI7PV4WAhos5tYXlxZ5e8dqsRz_zp4sr60-Ae1FMz8KoHibJlv9tjahBP5igIqerMmnQFD3FsXa6W5uC8F-ZYxk0fs8zQaq9dvG4q2jKUPkC5EvOmafYSFzoCUnylCBjkRgqC_Tw51ytBTQw7VE2Y1DdXF_-0Xd8tPmagZULZcxTK9A?width=5472&height=3648&cropmode=none')
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
    font-family: "Microsoft JhengHei UI"
  .company-subtitle
    margin-bottom: 1.35rem
    color: whitesmoke
    font-family: Bahnschrift
  .thick-bar
    margin-top: 1rem
  .customed-item
    color: whitesmoke
  .customed-item:hover
    color: #3273dc
    background-color: rgba(255, 255, 255, 0)
  .language
    color: whitesmoke
    margin-bottom: 0
  .navbar-link:hover
    .language
      color: #3273dc
    color: #3273dc
    background-color: rgba(255, 255, 255, 0)
  .flag
    padding-right: 0.5rem
</style>
