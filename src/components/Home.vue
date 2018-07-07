<template>
  <div>
    <section class="hero is-medium">
      <div class="hero-body about-hero-body">
        <div class="container has-text-centered">
          <h1 class="title is-size-1 about-title">
            20年电子产品制造经验
          </h1>
          <h2 class="subtitle about-subtitle">
            20 Years of Electronics Manufacturing Experience
          </h2>
          <p>成立于1999年,公司成立之始就定位为电子行业提供全新服务的科技型企业，公司现有员工600人。
          我们承揽电子产品类的OEM、ODM生产加工和制造,涉及消费电子、汽车电子、IT通信、IP电话、安防、医疗等各个领域，
          服务范围涉及工艺设计、物流配套、电路板贴片、焊接组装、可靠性测试及包装运输、进出口报关等,我们以提供全方位、全过程以及最全面和贴身的客户服务作为使命。</p>
        </div>
      </div>
    </section>
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
                专门为其生产OEM电子设备。
              </h2>
            </div>
            <div class="column">
              TEST
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="hero is-primary is-medium">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Service Provided Jumbotron
          </h1>
          <h2 class="subtitle">
            Large subtitle
          </h2>
        </div>
      </div>
    </section>
    <section class="hero is-info is-large">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Product Jumbotron
          </h1>
          <h2 class="subtitle">
            Large subtitle
          </h2>
        </div>
      </div>
    </section>
    <section class="hero">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title is-size-1 slogan-title">
            全力以赴，不断进步!
          </h1>
          <h2 class="subtitle is-pulled-right">
            ———— 创始人 & CEO， 苏华新
          </h2>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    created(){
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
  }
</script>

<style scoped>
  .about-title {
    font-family: shanhun;
  }
  .about-subtitle {
    font-family: Bahnschrift;
  }
  .hero.is-medium .hero-body.about-hero-body {
    padding-top: 5rem;
    padding-bottom: 5rem;
    background: whitesmoke;
  }
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
  .slogan-title {
    font-family: shanhun;
  }
  .subtitle-within {
    font-family: Bahnschrift;
    color: white;
  }
</style>
