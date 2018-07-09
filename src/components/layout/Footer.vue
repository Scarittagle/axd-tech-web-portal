<template>
  <footer class="footer">
    <div class="container">
      <div class="columns is-centered">
        <div class="column copy-right-title is-two-fifths is-paddingless">
          <h2 class="subtitle is-pulled-right">
            © {{ year }} 深圳市奥兴达科技有限公司
          </h2>
        </div>
        <div class="column is-narrow vertical-bar"/>
        <div class="column is-two-fifths is-narrow is-paddingless">
          <h1 class="title">
            联系我们
          </h1>
          <h2 class="subtitle">
            <fa-icon
              class="icon-color"
              icon="phone"/>
            电话：0755-3326 6975 或 13602573153 (CEO办公室)
          </h2>
          <h2 class="subtitle">
            <fa-icon
              class="icon-color"
              icon="at"/>
            邮箱：axd@axd-cn.com
          </h2>
          <h2 class="subtitle">
            <fa-icon
              class="icon-color"
              icon="window-maximize"/>
            网址：www.axd-cn.com
          </h2>
          <a
            class="subtitle map-link"
            @click="openMap">
            <fa-icon
              class="icon-color"
              icon="map-marked-alt"/>
            地址：深圳市光明新区蒋石油麻岗港深高新科技园B4/B5栋
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
  export default {
    computed: {
      year() {
        return new Date().getFullYear();
      },
    },
    methods: {
      openMap() {
        window.open('https://uri.amap.com/marker?position=113.893545,22.741849', '_blank');
      }
    }
  };
</script>

<style scoped>
  .title {
    margin-bottom: 2rem;
  }
  .subtitle {
    margin-bottom: 0;
  }
  .copy-right-title {
    margin-top: auto;
  }
  .vertical-bar {
    border-left: 5px darkgray solid;
    margin-left: 1.5rem;
  }
  .icon-color {
    color: #3273dc
  }
  .map-link:hover {
    color: #3273dc
  }
</style>
