<template>
  <section class="hero is-medium machine">
    <div class="hero-body">
      <div class="container">
        <div class="columns is-centered">
          <div class="column">
            <div class="columns is-vcentered">
              <div class="column">
                <div class="is-pulled-right">
                  <img
                    style="opacity: 0.9"
                    src="/static/collabrators/juki.png">
                </div>
              </div>
            </div>
            <div class="columns is-vcentered">
              <div class="column has-text-centered">
                <h1 class="title is-size-1 machine-title">
                  &
                </h1>
              </div>
            </div>
            <div class="columns is-vcentered">
              <div class="column">
                <div class="is-pulled-right">
                  <img
                    style="opacity: 0.9"
                    src="/static/collabrators/okinternational.png">
                </div>
              </div>
            </div>
            <div class="columns is-vcentered">
              <div class="column has-text-centered">
                <h1 class="title is-size-1 machine-title">
                  &
                </h1>
              </div>
            </div>
            <div class="columns is-vcentered">
              <div class="column">
                <div class="is-pulled-right">
                  <img
                    style="opacity: 0.9"
                    src="/static/collabrators/heller.png">
                </div>
              </div>
            </div>
          </div>
          <div class="column has-text-centered"/>
          <div class="column">
            <div class="is-pulled-left">
              <h1 class="title is-size-1 machine-title is-marginless">
                日本+美国
              </h1>
              <h1 class="title is-size-1 machine-title">
                进口机械科技
              </h1>
              <h2 class="subtitle machine-subtitle">
                Japan & United States Imported Machinery
              </h2>
              <h2 class="subtitle machine-content">
                我们拥有十几条SMT加工生产线，还有多条插件线、组装线及测试线。
                并且拥有全新的JUKI FX-3TL、JUKI KE-2070、JUKI KE-2080系列等新型中高速贴片机设备，
                多台九温区、十三温区HELLER回流焊炉和最新无铅波峰焊，还具有AOI检测设备以及美国OK公司的BGA返修系统等重要技术。
              </h2>
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
  .hero.is-medium.machine {
    background-image: url(/static/smtmachine.jpg);
    position: relative;
    background-size: cover;
  }
  .hero.is-medium.machine:before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background: rgba(0,0,0,0.7);
    opacity: 0.8
  }
  .machine-title {
    font-family: "Microsoft JhengHei UI";
    color: white;
  }
  .machine-subtitle {
    font-family: Bahnschrift;
    color: white;
  }
  .machine-content {
    font-family: "Microsoft JhengHei UI";
    color: white;
  }
</style>
