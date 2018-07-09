<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <div class="columns">
          <div class="column is-paddingless">
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
                <p class="subtitle err-msg">{{ error_message }}</p>
                <p class="subtitle">{{ notification_message }}</p>
              </template>
            </div>
            <div v-if="isSubmit">
              <h2 class="subtitle">感谢您提交表单，我们的工作人员将会在收到后的24小时内回复您。如果您没有收到回复的话，可以尝试使用电话联系我们公司。</h2>
              <h2 class="subtitle">此页面将会在5秒后跳转至首页...</h2>
            </div>
          </div>
          <div class="column map-custom-padding">
            <div class="amap-wrapper">
              <el-amap
                id="axd-location"
                class="amap-box"/>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  import * as emailjs from 'emailjs-com'
  import { lazyAMapApiLoaderInstance } from 'vue-amap'

  export default {
    data(){
      return{
        isSubmit: false,
        contactForm:{
          email: '',
          name: '',
          message: ''
        },
        error_message: null,
        notification_message: null,
      }
    },
    mounted() {
      const loadPromise = lazyAMapApiLoaderInstance.load();
      loadPromise.then(() => {
        this.map = new AMap.Map('axd-location', {
          zoomEnable:false,
          dragEnable: false,
          center: [113.893545, 22.741849],
          zoom: 16,
          lang: 'zh_cn',
        })
        AMapUI.loadUI(['overlay/SimpleInfoWindow'], (SimpleInfoWindow) => {
          const infoWindow = new SimpleInfoWindow({
            infoTitle: '<strong>奥兴达科技有限公司</strong>',
            infoBody: '<p>深圳市光明新区蒋石油麻岗港深高新科技园B4/B5栋</p>',
            map: this.map,
            position: this.map.getCenter()
          });
        });
      })
    },
    created(){
      window.scrollTo({
        top: 600,
        behavior: "smooth"
      });
    },
    methods:{
      submit() {
        this.error_message = null;
        if (this.contactForm.email !== '' && this.contactForm.name !== '' && this.contactForm.message !== '') {
          this.notification_message = '提交中,请稍后...';
          // TODO: EmailJS implementation
          emailjs.init("user_2JIyPb5ktoJn1om31lImh");
          const service_id = "default_service";
          const template_id = "template_HUBND88Y";
          const template_params = {
            "message_html": `<p>邮件地址： ${ this.contactForm.email }</p>
                             <p>姓名： ${ this.contactForm.name }</p>
                             <p>消息： ${ this.contactForm.message }</p>`,
          }

          emailjs.send(service_id, template_id, template_params)
            .then((response) => {
              console.log('SUCCESS!', response.status, response.text);
              this.isSubmit = true;
              setTimeout(() => {
                this.$router.push('/');
              }, 5000);
            }, (error) => {
              this.notification_message = null;
              this.error_message = error;
            });
        } else {
          this.error_message = '请填写完所有项再提交!';
        }
      },
    }
  }
</script>

<style scoped>
  .amap-wrapper {
    width: 100%;
    height: 100%;
  }
  .map-custom-padding {
    padding-left: 3rem;
    padding-right: 0;
    padding-top: 0;
    padding-bottom: 0;
  }
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
  .err-msg {
    margin-top: 2rem;
    color: red;
  }
</style>
