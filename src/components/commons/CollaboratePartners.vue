<template>
  <section class="hero is-medium">
    <div class="hero-body coop-company">
      <div class="container">
        <div class="columns">
          <div class="column is-two-fifths">
            <h1 class="title is-size-1 coop-company-title">
              合作厂商
              <br>
              <p class="subtitle subtitle-within">Collaborative partners</p>
            </h1>
            <h2 class="subtitle is-marginless coop-company-subtitle">
              我们与国内外许多电子品牌及厂商都有合作,
            </h2>
            <h2 class="subtitle coop-company-subtitle">
              专门为其生产OEM电子设备或者提供电子零部件
            </h2>
          </div>
          <div class="column">
            <div class="columns is-marginless">
              <div class="column">
                <img
                  width="70%"
                  height="70%"
                  class="is-pulled-right"
                  style="opacity: 0.7"
                  src="/static/collabrators/bestek.png">
              </div>
            </div>
            <div class="columns is-marginless">
              <div class="column">
                <img
                  class="is-pulled-right"
                  style="opacity: 0.7"
                  src="/static/collabrators/mcdevices.png">
              </div>
            </div>
            <div class="columns is-marginless">
              <div class="column">
                <img
                  width="50%"
                  height="50%"
                  class="is-pulled-right"
                  style="opacity: 0.7"
                  src="/static/collabrators/elite.png">
              </div>
            </div>
          </div>
          <div class="column">
            <div class="columns is-marginless">
              <div class="column">
                <h1
                  style="color: white; opacity: 0.7"
                  class="title is-pulled-right">安悦电子</h1>
              </div>
            </div>
            <div class="columns is-marginless">
              <div class="column">
                <img
                  width="50%"
                  height="50%"
                  class="is-pulled-right"
                  style="opacity: 0.7"
                  src="/static/collabrators/motorola.png">
              </div>
            </div>
            <div class="columns is-marginless">
              <div class="column">
                <img
                  width="50%"
                  height="50%"
                  class="is-pulled-right"
                  style="opacity: 0.7"
                  src="/static/collabrators/motorolasolutions.png">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
  }
</script>

<style scoped>
  .hero.is-medium .hero-body.coop-company {
    padding-top: 3rem;
    padding-bottom: 3rem;
    background-color: #38404c;
  }
  .coop-company-title {
    font-family: "Microsoft JhengHei UI";
    margin-bottom: 2rem;
    color: white;
  }
  .coop-company-subtitle {
    font-family: "Microsoft JhengHei UI";
    color: white;
  }
  .subtitle-within {
    font-family: Bahnschrift;
    color: white;
  }
</style>
