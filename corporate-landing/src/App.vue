<template>
  <div id="app">
    <Header :links="links"></Header>
    <Main
      :pricingInfos="pricingInfos"
      :articlesInfos="articlesInfos"
      :services="services"
      :workDetails="workDetails"
    ></Main>
    <Footer :links="links"></Footer>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Main from "@/components/Main.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      links: [
        {
          name: "Home",
          url: "#",
        },
        {
          name: "About",
          url: "#",
        },
        {
          name: "Services",
          url: "#",
        },
        {
          name: "Blog",
          url: "#",
        },
        {
          name: "Contact",
          url: "#",
        },
        {
          name: "Portfolio",
          url: "#",
        },
      ],
      pricingInfos: [
        {
          service: "Designing",
          forWho: "PROCESS",
          price: 40,
          detailOne: "Creative Design Enabled",
          detailTwo: "Vibrant Color Usage",
          detailThree: "Eye Catching Design",
          detailFour: "Extreme Typography",
          detailFive: "Exceptional Design",
          backgroundClass: "",
          backgroundButton: "pink-button",
        },
        {
          service: "Developing",
          forWho: "PRODUCT",
          price: 60,
          detailOne: "Creative Design Enabled",
          detailTwo: "Vibrant Color Usage",
          detailThree: "Eye Catching Design",
          detailFour: "Extreme Typography",
          detailFive: "Exceptional Design",
          backgroundClass: "pink-card",
          backgroundButton: "white-back",
        },
        {
          service: "Supporting",
          forWho: "CLIENTS",
          price: 80,
          detailOne: "Creative Design Enabled",
          detailTwo: "Vibrant Color Usage",
          detailThree: "Eye Catching Design",
          detailFour: "Extreme Typography",
          detailFive: "Exceptional Design",
          backgroundClass: "",
          backgroundButton: "pink-button",
        },
      ],
      articlesInfos: [
        {
          time: "April 21,2019",
          title:
            "Clearting Corporations get SEBI not to invest in overnight funds",
          text: " When, while the lovely valley teems with vapor around me, and the meridiana sun s...",
        },
        {
          time: "April 21,2019",
          title:
            "Shabnam Dhillion, wife of RSSB chief Gurinder Dhillon, passes away in London",
          text: " When, while the lovely valley teems with vapor around me, and the meridiana sun s...",
        },
      ],
      services: [
        {
          url: require("@/assets/img/Group-247.png"),
          name: "Data Analysis",
          text: " When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
        },
        {
          url: require("@/assets/img/Group-567.png"),
          name: "SEO Optimizazion",
          text: " When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
        },
        {
          url: require("@/assets/img/Group-538.png"),
          name: "Security Data",
          text: " When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
        },
        {
          url: require("@/assets/img/Group-566.png"),
          name: "Branding Strategy",
          text: " When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
        },
      ],
      workDetails: [
        {
          url: require("@/assets/img/DRY-1-790x576.jpg"),
          titleWork: "Basket of Flower on Table",
          serviceType: "Branding Strategy",
        },
        {
          url: require("@/assets/img/8wa60okr-1-790x576.jpg"),
          titleWork: "Purinky Products",
          serviceType: "Digital Experience",
        },
        {
          url: require("@/assets/img/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg"),
          titleWork: "Satisfy Poster",
          serviceType: "Branding Strategy",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "assets/scss/style.scss";
</style>