<template>
  <footer class="footer pb-5">
    
  </footer>
</template>
<script>
export default {
  props: {},
  data: function () {
    return {
      content: "",
      sitename: "",
      disclaimer: "",
      copyright: "",
      license: "",
      codeofconduct: "",
      footerLogo: false,
      footerLogoLink: "",
    };
  },
  components: {},
  methods: {},
  beforeMount(){
    this.sitename = document.getElementsByTagName("title")[0].innerText;
  },
  mounted() {
    this.copyright = window.themeOptions.footer_data.copyright;
    this.disclaimer = window.themeOptions.footer_data.disclaimer;
    this.license = window.themeOptions.footer_data.license;
    this.codeofconduct = window.themeOptions.footer_data.license;
    this.footerLogo = window.themeOptions.footer_data.footer_logo
    if(this.footerLogo){
      this.footerLogoLink = window.themeOptions.footer_data.footer_logo_link;
    } else {
      this.footerLogoLink = "";
    }
  },
};
</script>
