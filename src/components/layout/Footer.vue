<template>
  <footer class="footer">
    <div class="container">
      <div
        class="content has-text-centered">
        <div class="level">
          <div class="level-item">
            <p style="margin-bottom: unset;">
              © {{ year }} 深圳市奥兴达科技有限公司
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
  export default {
    data(){
      return {
        linkedin: 'https://www.linkedin.com/in/scarittagle/',
      }
    },
    computed: {
      year() {
        return new Date().getFullYear();
      },
    },
  };
</script>
