<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <h1 class="title contact-title">
          联系表单
        </h1>
        <h2 class="subtitle en-translate-contact-title">
          Contact Form
        </h2>
        <div v-if="!isSubmit">
          <h2 class="subtitle contact-subtitle">
            如果您对我司有任何疑问，合作意向，以及工作机会，您可以填写下列表单然后提交。提交后我司工作人员收到后会尽快的给您答复。
          </h2>
          <template>
            <hr>
            <section>
              <b-field label="姓名 Name：">
                <b-input
                  v-model="contactForm.name"
                  class="name"
                  type="text"
                  required/>
              </b-field>
              <b-field
                label="邮件地址 Email：">
                <b-input
                  v-model="contactForm.email"
                  class="email"
                  type="email"
                  maxlength="30"
                  required/>
              </b-field>
              <b-field label="消息内容 Message：">
                <b-input
                  v-model="contactForm.message"
                  maxlength="400"
                  type="textarea"
                  required/>
              </b-field>
            </section>
            <div
              class="button is-info is-outlined submit-button"
              @click="submit">
              提交
            </div>
          </template>
        </div>
        <div v-if="isSubmit">
          <h2 class="subtitle">感谢您提交表单，我们的工作人员将会在收到后的24小时内回复您。如果您没有收到回复的话，可以尝试使用电话联系我们公司。</h2>
          <h2 class="subtitle">此页面将会在5秒后跳转至首页...</h2>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  import router from 'vue-router'

  export default {
    data(){
      return{
        isSubmit: false,
        contactForm:{
          email: '',
          name: '',
          message: ''
        }
      }
    },
    created(){
      window.scrollTo({
        top: 600,
        behavior: "smooth"
      });
    },
    methods:{
      submit() {
        console.log(this.contactForm);
        // TODO: EmailJS implementation
        this.isSubmit = true;
        setTimeout(() => {
          this.$router.push('/');
        }, 5000);
      },
    }
  }
</script>

<style scoped>
  .contact-title {
    font-family: "Microsoft JhengHei UI";
  }
  .en-translate-contact-title {
    font-family: Bahnschrift;
  }
  .contact-subtitle {
    font-family: "Microsoft JhengHei UI";
  }
  .submit-button {
    width: 10rem;
  }
  .name {
    width: 20rem;
  }
  .email {
    width: 20rem;
  }
</style>
